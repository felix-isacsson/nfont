add_compile_definitions(FC_USE_SDL_GPU)

add_library(nfont
    STATIC
    NFont/NFont.cpp
    SDL_FontCache/SDL_FontCache.c
)

target_include_directories(nfont
    PUBLIC
    SDL_FontCache
)

target_link_libraries(nfont
    PUBLIC
    SDL2_ttf
)

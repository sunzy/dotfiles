syntax on
if !has('gui_running')
	let g:solarized_termtrans=1
	let g:solarized_termcolors=256
	set background=dark
endif
colorscheme solarized

set nocompatible              " be iMproved, required
filetype off                  " required
set completeopt-=preview

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

if filereadable(expand("~/.vimrc.bundles"))
    source ~/.vimrc.bundles
endif

call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line
"
set hls
set nocompatible
"状态栏
set laststatus=2
"设置编码
"set encoding=utf-8  
"设置文件编码
"set fenc=utf-8
"设置文件编码检测类型及支持格式(fencs = fileencodings)
set fencs=ucs-bom,utf-8,gb18030,gbk,gb2312,cp936,latin1
set number
"set relativenumber
set backspace=2
set backspace=indent,eol,start
"忽略大小写查找
set ic

"tab宽度
set tabstop=4
set cindent shiftwidth=4
set autoindent shiftwidth=4
"自动将tab转成空格
set expandtab

"设置代码折叠 manual/indent/expr/syntax/diff/marker

"手工/缩进/表达式/语法高亮/没有更改的文本/标志
set foldmethod=indent
"默认不折叠
set foldlevelstart=99

"自定义mapleader
let mapleader=","
let g:mapleader=","

"NERDTree
:map <leader>n :NERDTree<CR>
let NERDTreeQuitOnOpen=1
let NERDChristmasTree=1
let g:NERDTreeWinSize=32
map <leader>t :NERDTreeToggle<CR>
map <leader>r :NERDTreeFind<CR>
map <leader>bs :BookmarkToRoot static<CR>
map <leader>bw :BookmarkToRoot www2011<CR>
map <leader>bt :BookmarkToRoot test<CR>
map <leader>bi :BookmarkToRoot include<CR>
map <leader>bu :BookmarkToRoot ued<CR>
map <leader>bk :BookmarkToRoot trunk<CR>
map <leader>ba :BookmarkToRoot apps<CR>
map <leader>bp :BookmarkToRoot passport<CR>


"Tagbar
map <leader>g :TagbarToggle<CR>

"ctrlp
set wildignore+=*/tmp/*,*.so,*.swp,*.zip
let g:ctrlp_working_path_mode = 'ra'
let g:ctrlp_max_files=0
let g:ctrlp_max_depth=60
nnoremap <C-p> :CtrlPMRU<CR>

"MatchTagAlways
nnoremap <leader>% :MtaJumpToOtherTag<cr>

:map <leader>w <C-W>w
let g:user_zen_settings={
  \  'php' : {
  \    'extends' : 'html',
  \    'filters' : 'c',
  \  },
	\  'xml' : {
  \    'extends' : 'html',
  \},
\  'haml' : {
  \    'extends' : 'html',
  \  },
			\  'erb' : {
  \    'extends' : 'html',
  \  },
  \}



"SuperTab
let g:SuperTabRetainCompletionType="context"

"设置neocomplete启动时加载
let g:neocomplete#enable_at_startup = 1

"开启AutoPairs的FlyMode
let g:AutoPairsFlyMode = 1

"配置vim-deploy
if filereadable(expand("~/.vimrc.deploy.configs"))
    source ~/.vimrc.deploy.configs
endif

"ctags
set tags+=~/Project/mfw/build/trunk/tags
"这个自动保存的配置不会区分项目，建议以后改为匹配项目的
"autocmd BufWritePost * call system("ctags -R")

let g:vimwiki_list = [
            \{"path":"~/vimwiki","path_html":"~/vimwiki_html","syntax":"markdown","auto_export":0},
        \]



"Cscope

if has("cscope")
    if filereadable("cscope.out")
        cs add cscope.out
    elseif $CSCOPE_DB != ""
        cs add $CSCOPE_DB
    endif
endif

nnoremap <leader>fa :call cscope#findInteractive(expand('<cword>'))<CR>
nnoremap <leader>l :call ToggleLocationList()<CR>
" s: Find this C symbol
nnoremap  <leader>fs :call cscope#find('s', expand('<cword>'))<CR>
" g: Find this definition
nnoremap  <leader>fg :call cscope#find('g', expand('<cword>'))<CR>
" d: Find functions called by this function
nnoremap  <leader>fd :call cscope#find('d', expand('<cword>'))<CR>
" c: Find functions calling this function
nnoremap  <leader>fc :call cscope#find('c', expand('<cword>'))<CR>
" t: Find this text string
nnoremap  <leader>ft :call cscope#find('t', expand('<cword>'))<CR>
" e: Find this egrep pattern
nnoremap  <leader>fe :call cscope#find('e', expand('<cword>'))<CR>
" f: Find this file
nnoremap  <leader>ff :call cscope#find('f', expand('<cword>'))<CR>
" i: Find files #including this file
nnoremap  <leader>fi :call cscope#find('i', expand('<cword>'))<CR>

"列宽限制条
set colorcolumn=119

"copy file path
nnoremap <leader>fp :let @*=expand("%")<CR>

"snippets
let g:UltiSnipsExpandTrigger="<tab>"
let g:UltiSnipsJumpForwardTrigger="<c-b>"
let g:UltiSnipsJumpBackwardTrigger="<c-z>"
let g:UltiSnipsListSnippets="<c-tab>"
let g:UltiSnipsEditSplit="vertical"
nnoremap <leader>es :UltiSnipsEdit<CR>


"DiffOrig
nmap <leader>do <plug>diffo_open
nmap <leader>dx <plug>diffo_close
nmap <leader>du <plug>diffo_update

/* 
 * Yes, this codebase is near unreadable. Why?
 * I designed this mainly as a test to see how viable avoidance of straight out class selectors would be.
 * The codebase was never designed to be pretty, it was designed to require as little maintenance as possible.
 */

@import url('https://fonts.googleapis.com/css2?family=Karla:wght@400;500;600;700&display=swap');
@import url('https://mwittrien.github.io/BetterDiscordAddons/Themes/BlurpleRecolor/BlurpleRecolor.css');
@import url('https://discord-custom-covers.github.io/usrbg/dist/usrbg.css');

button {
	--accentcolor: var(--accent-alt);
}


/* Root Variables */

:root {
	--font-primary: 'Karla', sans-serif;
	--font-display: var(--font-primary) !important;
	/* Dark Matter Variables */
	--avatar-size: 32px;
	--background-image: url('https://i.imgur.com/7SbtKvw.png');
	--home-image: url('https://i.imgur.com/233d55Y.gif');
	--background-solid: #161921;
	--background-solid-dark: #101218;
	--background-solid-darker: #0c0e12;
	--accent: 37, 172, 232;
	--accent-alt: 29, 101, 134;
	--md-black: 0, 0, 0;
	--dm-white: 255, 255, 255;
	/* BlurpleRecolor */
	--accentcolor: var(--accent);
	--vaccentcolor-hover: rgb(var(--accent));
	--vaccentcolor-active: rgb(var(--accent));
}

:not(div[class*="userProfile"][class*="unThemed"]).theme-dark,
:not(div[class*="userProfile"]).theme-light,
div[class*="userProfile"][class*="unThemed"].theme-light {
	/* Discord vars */
	--background-primary: var(--background-solid);
	--background-mobile-primary: var(--background-primary);
	--background-secondary: var(--background-solid);
	--background-mobile-secondary: var(--background-secondary);
	--background-secondary-alt: var(--background-solid);
	--background-tertiary: var(--background-solid);
	--background-floating: var(--background-solid);
	--background-secondary: var(--background-solid);
	--background-accent: var(--background-solid);
	--background-message-hover: rgba(var(--md-black), 0.4);
	--channeltextarea-background: transparent;
	--activity-card-background: rgba(var(--dm-white), 0.05);
	--deprecated-store-bg: transparent;
	--background-modifier-hover: rgba(var(--md-black), 0.3);
	--background-modifier-active: rgba(var(--md-black), 0.3);
	--background-modifier-selected: rgba(var(--md-black), 0.6);
	--elevation-low: inset 0 -1px 0 0 rgba(var(--md-black), 0.3);
	--channels-default: rgba(var(--dm-white), 0.3);
	--deprecated-quickswitcher-input-background: var(--background-solid);
	--header-primary: rgba(var(--dm-white), 1);
	--header-secondary: rgba(var(--dm-white), 0.6);
	--text-normal: rgba(var(--dm-white), 0.6);
	--text-muted: #8a8e94;
	--interactive-muted: rgba(var(--dm-white), 0.15);
	--interactive-normal: rgba(var(--dm-white), 0.5);
	--interactive-hover: rgba(var(--dm-white), 0.75);
	--interactive-active: rgba(var(--dm-white), 1);
	--deprecated-card-bg: rgba(var(--dm-white), 0.05);
	--text-link: rgba(var(--accent), 1);
	--focus-primary: rgba(var(--accent), 1);
    --modal-background: var(--background-solid);
    --modal-footer-background: var(--background-solid-darker);
}

::selection {
	background-color: rgba(var(--accent-alt), 0.5);
}


/* Scrollbars */

::-webkit-scrollbar {
	width: 14px !important;
}

 ::-webkit-scrollbar-thumb {
	border-radius: 8px !important;
	border: 3px solid transparent !important;
	background-color: rgba(var(--accent-alt), 1) !important;
}

 ::-webkit-scrollbar-track {
	visibility: visible !important;
	border-radius: 8px !important;
	border: 3px solid transparent !important;
	background-color: rgba(0, 0, 0, 0.3) !important;
	background-clip: padding-box !important;
}

.none-2Eo-qx::-webkit-scrollbar {
	display: none !important;
}


/* Titlebar */

div[class*="typeWindows-"] {
	--background-modifier-hover: rgba(var(--dm-white), 0.05);
	--background-modifier-active: rgba(var(--dm-white), 0.075);
	height: 26px;
}

div[class*="typeWindows-"]>div:first-child {
	display: none;
}

div[class*="typeWindows-"]>div[role="button"] {
	height: 30px;
	width: 36px;
}

div[class*="typeWindows-"]::after {
	content: 'Discord';
	font-weight: 5000;
	line-height: 31px;
	color: var(--text-muted);
	font-size: 14px;
	position: absolute;
	padding: 0 12px;
	top: 0;
	left: 0;
	width: 100%;
	height: 30px;
	background: rgba(var(--md-black), 0.85);
	z-index: -1;
}


/* Guilds */

nav[class*="guilds-"] {
    background: transparent;
}
ul[data-list-id='guildsnav'] {
	--background-secondary: var(--background-solid);
    	--background-primary: rgba(var(--dm-white), 0.1);
	margin-bottom: 70px;
	background-color: rgba(var(--md-black), 0.6);
	border-right: 1px solid rgba(var(--md-black), 0.2);
	box-shadow: inset -10px 0px 20px -10px rgba(var(--md-black), 0.3);
}

ul[data-list-id='guildsnav'] ::-webkit-scrollbar {
	display: none;
}

ul[data-list-id='guildsnav']>div[dir] {
	padding-top: 18px;
}

ul[data-list-id='guildsnav'] [class^="pill-"],
ul[data-list-id='guildsnav'] [class^="pill-"]>div {
	height: 40px !important;
}

ul[data-list-id='guildsnav'] div[style*="height: 56"],
ul[id^="folder-items-"] {
	height: auto !important;
}

ul[data-list-id='guildsnav'] [class^="pill-"] span {
	width: 10px;
	margin-left: -5px;
	border-radius: 20px;
}

[data-list-id='guildsnav'] [class^="pill-"] span[style^="opacity: 1; height: 40"] {
	--header-primary: rgba(var(--accent), 1);
}

span[class^="expandedFolderBackground-"] {
	--background-secondary: rgba(var(--md-black), 0.25);
	border-radius: 14px;
	width: 40px;
	left: 16px;
}

.wrapper-28eC3z,
[data-list-id='guildsnav'] [data-dnd-name] > div,
[data-list-id='guildsnav'] svg[width="48"] {
	width: 40px;
	height: 40px;
}

div[data-list-item-id="guildsnav___home"] {
	background: var(--home-image) top center/110% no-repeat;
}

div[class^="unreadMentionsIndicatorBottom-"] {
	bottom: 70px;
}

#app-mount [data-list-item-id="guildsnav___home"]>div {
	color: transparent;
	background-color: transparent;
}

div[data-list-item-id="guildsnav___create-join-button"],
div[data-list-item-id="guildsnav___guild-discover-button"] {
	transition: 150ms ease;
	opacity: 0.5;
	background-color: var(--background-solid) !important;
	color: rgba(var(--dm-white), 0.3) !important;
	border: 1px dashed rgba(var(--dm-white), 0.3);
	border-radius: 50px;
}

div[data-list-item-id="guildsnav___create-join-button"]:hover,
div[data-list-item-id="guildsnav___guild-discover-button"]:hover {
	opacity: 1;
}


/* Sidebar */

.platform-win [class^="sidebar-"] {
	border-radius: 0;
    background-color: transparent;
}

div[class^="sidebar-"] nav,
#private-channels {
	background: var(--background-secondary) !important;
	--background-tertiary: rgba(var(--md-black), 0.35);
}

div[class^="sidebar-"]>nav>div[class^="searchBar"] {
	height: 54px;
}

/* members wrapper */
.container-2o3qEW {
	--background-secondary: rgba(var(--md-black), 0.4);
	--background-modifier-hover: rgba(var(--dm-white), 0.07);
	--background-modifier-active: var(--background-modifier-hover);
	--background-modifier-selected: rgba(var(--dm-white), 0.07);
    background: rgb(var(--md-black), 0.9);
}

div[data-list-id^="members-"][class*="scrollerBase-"] {
    background: transparent;
}

div[data-list-id^="members-"] [class*="placeholder"] {
	--backgorund-primary: var(--text-normal);
}

div[class^='nowPlayingColumn'] {
	--background-secondary: transparent;
	--background-primary: rgba(var(--md-black), 0.5);
	--background-modifier-hover: rgba(var(--dm-white), 0.075);
}
div[class^="members-"] div[class^="member-"] {
    background-color: transparent;
}

#channels div[class^="unread-"] {
	--interactive-active: rgba(var(--accent), 1);
}


/* Sidebar Header */

nav[aria-label]>div>header {
	display: flex;
	flex-direction: column;
	justify-content: center;
	height: 54px;
	--background-accent: rgba(var(--accent), 1);
	--background-modifier-hover: rgba(var(--md-black), 0.25);
}


/* Outer containers */

body {
	background: var(--background-image) center/cover no-repeat;
}

#app-mount {
    background-color: transparent;
	--background-tertiary: transparent;
	--background-secondary: transparent;
}

#app-mount>div[class^="appDevToolsWrapper-"] {
	--background-primary: transparent;
	--background-tertiary: transparent;
	--background-secondary: rgba(var(--md-black), 0.7);
	background-color: rgba(var(--md-black), 0.4);
}
div[class^="notAppAsidePanel-"]>div[class^="app-"]>div[class^="app-"],
div[class^="app-"]>div[class^="bg-"] {
    background-color: transparent;
}
div[class*="baseLayer-"]>div[class^="container-"] {
    background-color: rgb(var(--md-black), 0.4);
}

nav+div [class^='sidebar-'],
nav+div[class^='base-'] {
	overflow: visible !important;
	position: relative;
	max-width: calc(100% - 72px);
}

nav+div[class^='base-'] > div[class^="notice"] {
	border-radius: 0;
}

div[class^='base-']>div,
section[class*="themed-"] {
	--background-secondary: rgba(var(--md-black), 0.7);
	--background-tertiary: rgba(var(--dm-white), 0.05);
	--background-primary: rgba(var(--md-black), 0.8);
}

#app-mount>div:not([class^="appDevToolsWrapper-"]),
.autocomplete-1vrmpx {
	--background-primary: var(--background-solid);
	--background-secondary: var(--background-solid-dark);
	--background-secondary-alt: var(--background-solid-darker);
	--background-tertiary: var(--background-solid-darker);
}


/* Header */

section[class*="themed-"] {
	height: 54px;
	box-shadow: var(--elevation-low);
    background-color: rgb(var(--md-black), 0.925) !important;
	--background-secondary: rgba(var(--dm-white), 0.1);
}

section>div>a[href*="support.discord.com"] {
	display: none;
}

section[class*="themed-"]::before,
section[class*="themed-"] ::after {
	content: none;
}

section div[class^="toolbar"]>div[role] {
	margin: 0 4px;
	transition: 150ms ease;
	display: flex;
	align-items: center;
	justify-content: center;
	border-radius: 3px;
	width: 28px;
	height: 28px;
}

section div[class^="toolbar"]>div[role] svg {
	width: 22px;
}

section div[class^="toolbar"]>div[role][class*="selected-"] {
	background-color: rgba(var(--dm-white), 0.1);
}


/* Panels */

div[class^='sidebar-']>section {
	--background-primary: rgba(var(--dm-white), 0.07);
	--background-secondary: rgba(var(--dm-white), 0.1);
	--background-secondary-alt: rgba(var(--md-black), 0.95);
	margin-bottom: 70px;
}

div[class^='sidebar-']>section>div:last-child {
	background-color: var(--background-secondary-alt);
	box-sizing: border-box;
	height: 70px;
	padding: 0 18px;
	width: calc(100% + 72px);
	position: absolute;
	left: -72px;
	bottom: 0;
}
div[class^="sidebar-"]>section>div:last-child [class^="avatarWrapper-"] {
    flex: 1;
}


/* Content */

div[class^='chat'] {
	--background-floating: rgba(var(--md-black), 0.5);
    background: transparent;
}

div[class^="container-"][id^="chat-messages-"] {
	--background-modifier-hover: var(--background-solid-dark);
}

div[class^='chat'] main form {
	margin-top: 0;
}

div[class^='chat'] main form::before {
	content: none;
}

div[data-list-id="chat-messages"] {
	--background-primary: transparent;
	--background-secondary: rgba(var(--dm-white), 0.05);
	--background-accent: rgba(var(--dm-white), 0.1);
}

div[class^="channelTextArea-"] {
	--background-secondary: transparent;
	box-shadow: inset 0 0 0 2px rgba(var(--dm-white), 0.1);
	transition: 250ms ease;
	margin-bottom: 24px;
	margin-top: 12px;
	border-radius: 5px;
}

div[id^="chat-messages-"]+div:not([id]):last-child {
	height: 8px;
}

div[id^="chat-messages-"][class*="cozy-"] {
	padding-left: calc(var(--avatar-size) * 2);
}

div[id^="chat-messages-"] {
	margin-left: 8px;
	margin-right: 8px;
	border-radius: 4px;
}

div[id^="chat-messages-"]>div[class^="buttonContainer-"] {
	transform: scale(.85);
	top: 1px;
}

div[id^="chat-messages-"] {
	--background-primary: rgba(var(--md-black), 0.5);
}

div[id^="chat-messages-"]>div>[class^="avatar-"] {
	margin-top: 6px;
	width: var(--avatar-size);
	height: var(--avatar-size);
}

div[id^="chat-messages-"][class*="cozy-"] div::before {
	--gutter: 13px;
}

.mention {
	transition: 150ms ease;
	color: rgba(var(--accent), 1) !important;
	background-color: rgba(var(--accent), 0.3);
	padding: 3px 5px;
	border-radius: 5px;
}

.mention:hover {
	background-color: rgba(var(--accent), 0.3) !important;
}

#app-mount .container-2cd8Mz {
	background: var(--background-primary);
}

div[class*="barBase-"] {
	padding-bottom: 0;
	background-color: rgba(var(--accent-alt), 0.9);
}


/* Codeblocks */

html pre {
	border-radius: 0;
	background: transparent;
	border-color: rgba(255, 255, 255, 0.1);
}

pre code.hljs {
	border: none;
	background-color: rgba(var(--dm-white), 0.1);
	color: rgba(var(--dm-white), 0.7);
	padding: 1em;
}

html code.inline,
html code.inline {
	background: rgba(var(--dm-white), 0.1);
	color: rgba(var(--dm-white), 0.7);
	padding: 0.3em 0.6em;
	border-radius: 3px;
}


/* Settings */

div[aria-label*="_SETTINGS"],
div[aria-label*="_DEBUG"] {
	--background-primary: transparent;
	--background-secondary: rgba(var(--md-black), 0.7);
}

div[class^="sidebarRegionScroller-"]>nav {
	--background-secondary: transparent;
}

div[class^="contentRegion-"] {
	--background-primary: rgba(var(--md-black), 0.8);
}

div[class^="contentRegion-"] div[style^="overflow: hidden scroll"] {
	background-color: transparent;
	--background-primary: rgba(var(--md-black), 0.1);
	--background-secondary: rgba(var(--md-black), 0.2);
	--background-secondary-alt: rgba(var(--md-black), 0.25);
	--background-tertiary: rgba(var(--dm-white), 0.1);
}

div[aria-label*="_SETTINGS"] aside>div {
	--background-primary: transparent;
}

div[aria-label*="_SETTINGS"] aside>div::-webkit-scrollbar-track {
	visibility: hidden !important;
}

.bd-addon-list {
	--background-secondary: var(--background-solid);
	--background-secondary-alt: var(--background-solid-dark);
}


/* Tab Bar */

div[class*="topPill"],
nav>div[role="tablist"],
.bd-tab-bar {
	--background-accent: rgba(var(--accent));
	--background-modifier-hover: rgba(var(--dm-white), 0.05);
	--background-modifier-active: rgba(var(--dm-white), 0.075);
	--background-modifier-selected: rgba(var(--accent), 0.25);
}


/* Server Discovery */

div[class^="sidebar"]+[class^="pageWrapper"] {
	--background-secondary: rgba(var(--md-black), 0.8);
	background-color: var(--background-secondary);
}


/* Crash Page */

div[class*="errorPage"] {
	--background-secondary: rgba(var(--md-black), 0.7) !important;
}


/* Tooltips */

div[class^="tooltip-"] {
	--background-floating: rgba(var(--accent-alt), 1);
	--text-normal: #e0e0e0;
}


/* Buttons */

button[class*="button-"][class*="color"],
.bd-button {
	--vaccentcolor: var(--accent-alt);
}

.bd-button {
	--bd-blue: rgba(var(--accent-alt), 1);
}


/* Context Menu */

div[role="menuitem"] {
	--vaccentcolor: var(--accent-alt);
}

div[role="menuitem"]:active {
	--vaccentcolor: var(--accent);
}


/* Depreceated Components */


/* These use hardcoded colors, no need to bother with strange selectors */

#app-mount .footer-2gL1pp,
#app-mount .footer-3mqk7D {
	background-color: var(--background-secondary);
	box-shadow: none;
}

#app-mount .root-1gCeng,
#app-mount .addGamePopout-2RY8Ju,
#app-mount .keyboardShortcutsModal-3piNz7,
#app-mount .emojiAliasInput-1y-NBz .emojiInput-1aLNse,
.perksModal-fSYqOq .perk-2WeBWW,
#app-mount .uploadModal-2ifh8j,
#app-mount .contentWrapper-3WC1ID,
#app-mount .contentWarningPopout-n5JsIs {
	background-color: var(--background-primary);
}

#app-mount .codeRedemptionRedirect-1wVR4b,
#app-mount .userSettingsVoice-iwdUCU .previewOverlay-2O7_KC,
#app-mount .inset-3sAvek {
	background-color: var(--background-tertiary);
	border: none;
}

#app-mount .paymentPane-3bwJ6A,
#app-mount .tierBody-x9kBBp,
#app-mount .tierBody-16Chc9,
#app-mount .barBackground-2EEiLw,
#app-mount .body-3iLsc4,
#app-mount .footer-1fjuF6,
#app-mount .container-3ayLPN,
#app-mount .colorPickerCustom-2CWBn2,
#app-mount .tierMarkerBackground-3q29am,
.css-3vaxre-menu,
.css-dwar6a-menu,
#app-mount .autocomplete-1vrmpx,
.categoryHeader-O1zU94,
#app-mount .popoutList-T9CKZQ,
#app-mount .quickSelectPopout-X1hvgV,
.colorable-1bkp8v.primaryDark-3mSFDl,
.tile-2naSqK,
.videoWrapper-2v09vt,
#app-mount .spoilerText-3p6IlD.hidden-HHr2R9 {
	background-color: var(--background-solid);
}

#app-mount .expandedInfo-3kfShd,
#app-mount .tierHeaderLocked-1a2opw,
#app-mount .tierHeaderLocked-1s2JJz,
#app-mount .headerNormal-T_seeN,
#app-mount .focused-2bY0OD,
.colorable-1bkp8v.primaryDark-3mSFDl:hover {
	background-color: var(--background-solid-dark);
}

#app-mount .payment-xT17Mq {
	background-color: transparent;
	border-bottom-color: rgba(var(--dm-white), 0.025);
}

#app-mount .bottomDivider-1K9Gao,
#app-mount .focused-2bY0OD {
	border-bottom-color: var(--background-solid-dark);
}

#app-mount div[data-list-id="billing-history"],
#app-mount div[data-list-id^="private-channels-"],
#app-mount .media-engine-video,
.react-datepicker,
.react-datepicker__header,
.react-datepicker__day--outside-month,
.react-datepicker__day--disabled,
div[data-list-id^="members-"],
div[data-list-id^="members-"]>div {
	background-color: transparent !important;
}

.react-datepicker__day--disabled {
	opacity: .6;
}

#app-mount .react-datepicker__day {
	border-top-color: var(--background-secondary);
	border-left-color: var(--background-secondary);
}

#app-mount .background-3xPPFc,
#app-mount .tierInProgress-3mBoXq {
	color: var(--background-solid);
}

.option-96V44q:after {
	content: none;
}

#app-mount .option-96V44q.selected-rZcOL-,
#app-mount .selected-1Tbx07,
#app-mount .quickSelectPopoutOption-opKBx9:hover,
#app-mount .outer-1AjyKL.active-1xchHY,
#app-mount .outer-1AjyKL.interactive-3B9GmY:hover {
	background-color: var(--background-modifier-hover);
}

.css-3vaxre-menu,
.tierMarker-5HkGJ_[style] {
	border-color: rgba(var(--dm-white), 0.025) !important;
}

#app-mount .searchAnswer-3Dz2-q,
#app-mount .searchFilter-2ESiM3,
#app-mount .option-1B5ZV8,
#app-mount .pill-2pQByF {
	background-color: rgba(var(--accent-alt), 1);
	color: #fff;
}

#app-mount .keybindShortcut-1BD6Z1 span {
	background: var(--background-solid-dark);
	box-shadow: inset 0 -4px 0 var(--background-solid-darker);
}

#app-mount .perksModal-fSYqOq {
	background: rgba(var(--md-black), 0.7);
}

#app-mount .card-FDVird:before {
	background: var(--background-modifier-hover);
	border: none;
}


/* Login Page */

div[class^="splashBackground"] canvas,
div[class^="splashBackground"] img {
	display: none;
}

/* Modals */

div[class*="footerSeparator"] {
	box-shadow: none !important;
}

/* Forums */
.container-3wLKDe {
    background: var(--background-primary);
}
li[class^="card-"]>div[class^="container-"] {
    background: var(--background-floating)
}

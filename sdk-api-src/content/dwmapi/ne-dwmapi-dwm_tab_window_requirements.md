---
UID: NE:dwmapi.DWM_TAB_WINDOW_REQUIREMENTS
title: DWM_TAB_WINDOW_REQUIREMENTS (dwmapi.h)

description: Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.
old-location: dwm\dwm_tab_window_requirements.htm
tech.root: dwm
ms.assetid: 8366ABE4-263D-448D-9FC9-3F4DAF9B700D

ms.date: 12/05/2018
ms.keywords: DWMTWR_IMPLEMENTED_BY_SYSTEM, DWMTWR_NONE, DWMTWR_TABBING_ENABLED, DWMTWR_USER_POLICY, DWMTWR_WINDOW_DWM_ATTRIBUTES, DWMTWR_WINDOW_MARGINS, DWMTWR_WINDOW_REGION, DWMTWR_WINDOW_RELATIONSHIP, DWMTWR_WINDOW_STYLES, DWM_TAB_WINDOW_REQUIREMENTS, DWM_TAB_WINDOW_REQUIREMENTS enumeration [Desktop Window Manager], dwm.dwm_tab_window_requirements, dwmapi/ DWMTWR_WINDOW_STYLES, dwmapi/DWMTWR_IMPLEMENTED_BY_SYSTEM, dwmapi/DWMTWR_NONE, dwmapi/DWMTWR_TABBING_ENABLED, dwmapi/DWMTWR_USER_POLICY, dwmapi/DWMTWR_WINDOW_DWM_ATTRIBUTES, dwmapi/DWMTWR_WINDOW_MARGINS, dwmapi/DWMTWR_WINDOW_REGION, dwmapi/DWMTWR_WINDOW_RELATIONSHIP, dwmapi/DWM_TAB_WINDOW_REQUIREMENTS
ms.topic: enum
f1_keywords: 
 - "dwmapi/DWM_TAB_WINDOW_REQUIREMENTS"
dev_langs:
 - c++
req.header: dwmapi.h
req.include-header: Dwmmapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwmapi.h
api_name:
 - DWM_TAB_WINDOW_REQUIREMENTS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DWM_TAB_WINDOW_REQUIREMENTS enumeration


## -description


Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.


## -enum-fields




### -field DWMTWR_NONE

The window meets all requirements requested.


### -field DWMTWR_IMPLEMENTED_BY_SYSTEM

In some configurations, the admin/user setting or mode of the system means that windows won't be tabbed. This requirement indicates that the system mode must implement tabbing. If the system does not implement tabbing, nothing can be done to change this.



### -field DWMTWR_WINDOW_RELATIONSHIP

The window has an owner or parent, and is therefore ineligible for tabbing.


### -field DWMTWR_WINDOW_STYLES

    The window has one or more styles that make it ineligible for tabbing.


To be eligible for tabbing, a window must:

<ul>
<li>Have the <b>WS_OVERLAPPEDWINDOW</b> (such as <b>WS_CAPTION</b>, <b>WS_THICKFRAME</b>, etc.) styles set.</li>
<li>Not have <b>WS_POPUP</b>, <b>WS_CHILD</b> or <b>WS_DLGFRAME</b> set.</li>
<li>Not have <b>WS_EX_TOPMOST</b> or <b>WS_EX_TOOLWINDOW</b> set.
</li>
</ul>



### -field DWMTWR_WINDOW_REGION

The window has a region (set using <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowrgn">SetWindowRgn</a>) making it ineligible.


### -field DWMTWR_WINDOW_DWM_ATTRIBUTES

The window is ineligible due to its Dwm configuration.

To resolve this issue, the window must not extended its client area into the title bar using <a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea">DwmExtendFrameIntoClientArea</a>. In addition, the window must not have <b>DWMWA_NCRENDERING_POLICY</b> set to <b>DWMNCRP_ENABLED</b>. 


### -field DWMTWR_WINDOW_MARGINS

The window is ineligible due to its margins, most likely due to custom handling in <b>WM_NCCALCSIZE</b>. 

To resolve this issue, the window must use the default window margins for the non-client area.



### -field DWMTWR_TABBING_ENABLED

The window has been explicitly opted out by setting <b>DWMWA_TABBING_ENABLED</b> to false.


### -field DWMTWR_USER_POLICY

The user has configured this application to not participate in tabbing.


### -field DWMTWR_GROUP_POLICY


### -field DWMTWR_APP_COMPAT




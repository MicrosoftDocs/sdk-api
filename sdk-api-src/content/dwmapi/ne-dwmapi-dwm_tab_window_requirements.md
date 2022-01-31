---
UID: NE:dwmapi.DWM_TAB_WINDOW_REQUIREMENTS
title: DWM_TAB_WINDOW_REQUIREMENTS (dwmapi.h)
description: Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.
helpviewer_keywords: ["DWMTWR_IMPLEMENTED_BY_SYSTEM","DWMTWR_NONE","DWMTWR_TABBING_ENABLED","DWMTWR_USER_POLICY","DWMTWR_WINDOW_DWM_ATTRIBUTES","DWMTWR_WINDOW_MARGINS","DWMTWR_WINDOW_REGION","DWMTWR_WINDOW_RELATIONSHIP","DWMTWR_WINDOW_STYLES","DWM_TAB_WINDOW_REQUIREMENTS","DWM_TAB_WINDOW_REQUIREMENTS enumeration [Desktop Window Manager]","dwm.dwm_tab_window_requirements","dwmapi/ DWMTWR_WINDOW_STYLES","dwmapi/DWMTWR_IMPLEMENTED_BY_SYSTEM","dwmapi/DWMTWR_NONE","dwmapi/DWMTWR_TABBING_ENABLED","dwmapi/DWMTWR_USER_POLICY","dwmapi/DWMTWR_WINDOW_DWM_ATTRIBUTES","dwmapi/DWMTWR_WINDOW_MARGINS","dwmapi/DWMTWR_WINDOW_REGION","dwmapi/DWMTWR_WINDOW_RELATIONSHIP","dwmapi/DWM_TAB_WINDOW_REQUIREMENTS"]
old-location: dwm\dwm_tab_window_requirements.htm
tech.root: dwm
ms.assetid: 8366ABE4-263D-448D-9FC9-3F4DAF9B700D
ms.date: 12/05/2018
ms.keywords: DWMTWR_IMPLEMENTED_BY_SYSTEM, DWMTWR_NONE, DWMTWR_TABBING_ENABLED, DWMTWR_USER_POLICY, DWMTWR_WINDOW_DWM_ATTRIBUTES, DWMTWR_WINDOW_MARGINS, DWMTWR_WINDOW_REGION, DWMTWR_WINDOW_RELATIONSHIP, DWMTWR_WINDOW_STYLES, DWM_TAB_WINDOW_REQUIREMENTS, DWM_TAB_WINDOW_REQUIREMENTS enumeration [Desktop Window Manager], dwm.dwm_tab_window_requirements, dwmapi/ DWMTWR_WINDOW_STYLES, dwmapi/DWMTWR_IMPLEMENTED_BY_SYSTEM, dwmapi/DWMTWR_NONE, dwmapi/DWMTWR_TABBING_ENABLED, dwmapi/DWMTWR_USER_POLICY, dwmapi/DWMTWR_WINDOW_DWM_ATTRIBUTES, dwmapi/DWMTWR_WINDOW_MARGINS, dwmapi/DWMTWR_WINDOW_REGION, dwmapi/DWMTWR_WINDOW_RELATIONSHIP, dwmapi/DWM_TAB_WINDOW_REQUIREMENTS
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWM_TAB_WINDOW_REQUIREMENTS
 - dwmapi/DWM_TAB_WINDOW_REQUIREMENTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwmapi.h
api_name:
 - DWM_TAB_WINDOW_REQUIREMENTS
---

# DWM_TAB_WINDOW_REQUIREMENTS enumeration


## -description

Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.

## -enum-fields

### -field DWMTWR_NONE:0x0000

The window meets all requirements requested.

### -field DWMTWR_IMPLEMENTED_BY_SYSTEM:0x0001

In some configurations, the admin/user setting or mode of the system means that windows won't be tabbed. This requirement indicates that the system mode must implement tabbing. If the system does not implement tabbing, nothing can be done to change this.

### -field DWMTWR_WINDOW_RELATIONSHIP:0x0002

The window has an owner or parent, and is therefore ineligible for tabbing.

### -field DWMTWR_WINDOW_STYLES:0x0004

    The window has one or more styles that make it ineligible for tabbing.


To be eligible for tabbing, a window must:

<ul>
<li>Have the <b>WS_OVERLAPPEDWINDOW</b> (such as <b>WS_CAPTION</b>, <b>WS_THICKFRAME</b>, etc.) styles set.</li>
<li>Not have <b>WS_POPUP</b>, <b>WS_CHILD</b> or <b>WS_DLGFRAME</b> set.</li>
<li>Not have <b>WS_EX_TOPMOST</b> or <b>WS_EX_TOOLWINDOW</b> set.
</li>
</ul>

### -field DWMTWR_WINDOW_REGION:0x0008

The window has a region (set using <a href="/windows/desktop/api/winuser/nf-winuser-setwindowrgn">SetWindowRgn</a>) making it ineligible.

### -field DWMTWR_WINDOW_DWM_ATTRIBUTES:0x0010

The window is ineligible due to its Dwm configuration.

To resolve this issue, the window must not extended its client area into the title bar using <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea">DwmExtendFrameIntoClientArea</a>. In addition, the window must not have <b>DWMWA_NCRENDERING_POLICY</b> set to <b>DWMNCRP_ENABLED</b>.

### -field DWMTWR_WINDOW_MARGINS:0x0020

The window is ineligible due to its margins, most likely due to custom handling in <b>WM_NCCALCSIZE</b>. 

To resolve this issue, the window must use the default window margins for the non-client area.

### -field DWMTWR_TABBING_ENABLED:0x0040

The window has been explicitly opted out by setting <b>DWMWA_TABBING_ENABLED</b> to false.

### -field DWMTWR_USER_POLICY:0x0080

The user has configured this application to not participate in tabbing.

### -field DWMTWR_GROUP_POLICY:0x0100

### -field DWMTWR_APP_COMPAT:0x0200

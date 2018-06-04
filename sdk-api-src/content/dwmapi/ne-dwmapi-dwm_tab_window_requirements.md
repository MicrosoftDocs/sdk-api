---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

The window has a region (set using <a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a>) making it ineligible.


### -field DWMTWR_WINDOW_DWM_ATTRIBUTES

The window is ineligible due to its Dwm configuration.

To resolve this issue, the window must not extended its client area into the title bar using <a href="https://msdn.microsoft.com/4ea409df-3980-4903-b481-6ff718dc01bc">DwmExtendFrameIntoClientArea</a>. In addition, the window must not have <b>DWMWA_NCRENDERING_POLICY</b> set to <b>DWMNCRP_ENABLED</b>. 


### -field DWMTWR_WINDOW_MARGINS

The window is ineligible due to its margins, most likely due to custom handling in <b>WM_NCCALCSIZE</b>. 

To resolve this issue, the window must use the default window margins for the non-client area.



### -field DWMTWR_TABBING_ENABLED

The window has been explicitly opted out by setting <b>DWMWA_TABBING_ENABLED</b> to false.


### -field DWMTWR_USER_POLICY

The user has configured this application to not participate in tabbing.


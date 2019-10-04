---
UID: NN:shobjidl_core.IShellMenu
title: IShellMenu (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that interact with Shell menus such as the Start menu, and the Favorites menu.
old-location: shell\IShellMenu.htm
tech.root: shell
ms.assetid: 46793ae9-936e-4a58-bc34-84396151b4a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellMenu, IShellMenu interface [Windows Shell], IShellMenu interface [Windows Shell],described, _shell_IShellMenu, shell.IShellMenu, shobjidl_core/IShellMenu
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IShellMenu"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellMenu
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellMenu interface


## -description


Exposes methods that interact with Shell menus such as the <b>Start</b> menu, and the <b>Favorites</b> menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellMenu</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellMenu</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellMenu</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-getmenu">GetMenu</a>
</td>
<td align="left" width="63%">
Gets the menu information set by calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setmenu">IShellMenu::SetMenu</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-getmenuinfo">GetMenuInfo</a>
</td>
<td align="left" width="63%">
Gets information from the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-getshellfolder">GetShellFolder</a>
</td>
<td align="left" width="63%">
Gets the folder that the menu band is set to browse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-getstate">GetState</a>
</td>
<td align="left" width="63%">
Gets a filled <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-smdata">SMDATA</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a menu band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-invalidateitem">InvalidateItem</a>
</td>
<td align="left" width="63%">
Redraws an item in a menu band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setmenu">SetMenu</a>
</td>
<td align="left" width="63%">
Appends a static menu to the menu band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setmenutoolbar">SetMenuToolbar</a>
</td>
<td align="left" width="63%">
Adds a menu to the menuband.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setshellfolder">SetShellFolder</a>
</td>
<td align="left" width="63%">
Specifies the folder for the menu band to browse.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <i>rclsid</i> parameter set to CLSID_MenuBand and the <i>riid</i> parameter set to IID_IShellMenu. You must first initialize the interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-initialize">IShellMenu::Initialize</a>, and then initialize the menu band by calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenu-setshellfolder">IShellMenu::SetShellFolder</a>.




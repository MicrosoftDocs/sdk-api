---
UID: NN:shobjidl_core.IShellMenu
title: IShellMenu
author: windows-driver-content
description: Exposes methods that interact with Shell menus such as the Start menu, and the Favorites menu.
old-location: shell\IShellMenu.htm
old-project: shell
ms.assetid: 46793ae9-936e-4a58-bc34-84396151b4a3
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IShellMenu, IShellMenu interface [Windows Shell], IShellMenu interface [Windows Shell],described, _shell_IShellMenu, shell.IShellMenu, shobjidl_core/IShellMenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellMenu
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IShellMenu interface


## -description


Exposes methods that interact with Shell menus such as the <b>Start</b> menu, and the <b>Favorites</b> menu.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellMenu</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellMenu</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b366d9c9-5dd3-43ee-99a1-417b9d907855">GetMenu</a>
</td>
<td align="left" width="63%">
Gets the menu information set by calling <a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">IShellMenu::SetMenu</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/979d43ce-d8e6-444f-8082-49b52c0ad2ef">GetMenuInfo</a>
</td>
<td align="left" width="63%">
Gets information from the <a href="https://msdn.microsoft.com/dc9864df-21f3-4b0b-b862-48055032c071">IShellMenu::Initialize</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f88e1ee-950f-41b8-ad53-3bd7e8772f42">GetShellFolder</a>
</td>
<td align="left" width="63%">
Gets the folder that the menu band is set to browse.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea5d402f-2644-4e42-b1e7-2304f0ca71e2">GetState</a>
</td>
<td align="left" width="63%">
Gets a filled <a href="https://msdn.microsoft.com/4690daa1-f935-4d0c-8b1f-0b9442fc78dc">SMDATA</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a menu band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/694722f2-2030-4c85-bcc4-70f8a8b70161">InvalidateItem</a>
</td>
<td align="left" width="63%">
Redraws an item in a menu band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afa393eb-05a0-478e-88a2-7c31b4a48930">SetMenu</a>
</td>
<td align="left" width="63%">
Appends a static menu to the menu band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6067f2be-883a-4271-95ad-16fd868b37a0">SetMenuToolbar</a>
</td>
<td align="left" width="63%">
Adds a menu to the menuband.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b442f64a-c8ab-4431-87d9-481befb51af7">SetShellFolder</a>
</td>
<td align="left" width="63%">
Specifies the folder for the menu band to browse.

</td>
</tr>
</table> 


## -remarks



To get a pointer to this interface, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with the <i>rclsid</i> parameter set to CLSID_MenuBand and the <i>riid</i> parameter set to IID_IShellMenu. You must first initialize the interface by calling <a href="https://msdn.microsoft.com/dc9864df-21f3-4b0b-b862-48055032c071">IShellMenu::Initialize</a>, and then initialize the menu band by calling <a href="https://msdn.microsoft.com/b442f64a-c8ab-4431-87d9-481befb51af7">IShellMenu::SetShellFolder</a>.




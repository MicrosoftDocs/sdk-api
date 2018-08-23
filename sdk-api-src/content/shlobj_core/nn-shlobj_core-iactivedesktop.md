---
UID: NN:shlobj_core.IActiveDesktop
title: IActiveDesktop
author: windows-sdk-content
description: Allows a client program to manage the desktop items and wallpaper on a local computer.
old-location: lwef\iactivedesktop_interface.htm
old-project: lwef
ms.assetid: 4d572b86-36e8-417b-857c-eb477c04c691
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IActiveDesktop, IActiveDesktop interface [Legacy Windows Environment Features], IActiveDesktop interface [Legacy Windows Environment Features],described, _win32_IActiveDesktop_Interface, lwef.iactivedesktop_interface, shell.iactivedesktop_interface, shlobj_core/IActiveDesktop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# IActiveDesktop interface


## -description


Allows a client program to manage the desktop items and wallpaper on a local computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveDesktop</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IActiveDesktop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActiveDesktop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a0c61e8-a645-4a32-b97b-8d7b43d0e5e3">AddDesktopItem</a>
</td>
<td align="left" width="63%">
Adds a desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac582bd7-9fd1-4134-a866-69319ef3d96e">AddDesktopItemWithUI</a>
</td>
<td align="left" width="63%">
Adds a desktop item to the Active Desktop after  displaying user interfaces that confirm the addition of the desktop item, verifying security zone permissions, and asking if the user wants to create a subscription.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/295b2f46-6178-4aef-9721-8105c75a4a55">AddUrl</a>
</td>
<td align="left" width="63%">
Adds the desktop item associated with the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bac5af5-f4a6-4822-83de-11633beef88a">ApplyChanges</a>
</td>
<td align="left" width="63%">
Applies changes to the Active Desktop and saves them in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/653c9c92-4301-4960-b25e-e8e11f9d2fb8">GenerateDesktopItemHtml</a>
</td>
<td align="left" width="63%">
Generates a generic HTML page containing the given desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9d4a771-023f-4a31-b9b7-39b8b4a8695a">GetDesktopItem</a>
</td>
<td align="left" width="63%">
Gets the specified desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44e5fc48-b50d-4410-87c8-7e42634218bf">GetDesktopItemByID</a>
</td>
<td align="left" width="63%">
Gets the desktop item that matches the given identification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9449238a-c1af-493c-9c23-503317fe6656">GetDesktopItemBySource</a>
</td>
<td align="left" width="63%">
Gets a desktop item using its source URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2bba6f8-4ff0-4978-93ae-46db9ec6ea48">GetDesktopItemCount</a>
</td>
<td align="left" width="63%">
Gets a count of the desktop items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3717b67a-b028-44a9-af1c-a6a94b2d76d8">GetDesktopItemOptions</a>
</td>
<td align="left" width="63%">
Gets the options for the desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4211868-9f06-412c-b0b5-ba6ce395708e">GetPattern</a>
</td>
<td align="left" width="63%">
Gets the current pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b56cf857-5f3c-47f0-a1c2-e578c44c971b">GetWallpaper</a>
</td>
<td align="left" width="63%">
Gets the current wallpaper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b524a2b8-e6b6-4592-9435-88a6842b2338">GetWallpaperOptions</a>
</td>
<td align="left" width="63%">
Gets the wallpaper options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f80a0b49-3fa9-4041-833e-1e809a606a0c">ModifyDesktopItem</a>
</td>
<td align="left" width="63%">
Modifies the desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fee6c97-0605-4ad3-90fb-c5271f78536a">RemoveDesktopItem</a>
</td>
<td align="left" width="63%">
Removes the specified desktop item from the desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f2c1f41-d678-4eb8-b246-46133eec465f">SetDesktopItemOptions</a>
</td>
<td align="left" width="63%">
Sets the item's options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca66a200-dd12-454b-b449-feeae26941b6">SetPattern</a>
</td>
<td align="left" width="63%">
Sets the Active Desktop pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e789a8f1-3e65-4fa7-a62b-8fad6114ed46">SetWallpaper</a>
</td>
<td align="left" width="63%">
Sets the wallpaper for the Active Desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbe09c68-26f8-4db4-9e74-87f0a94c7918">SetWallpaperOptions</a>
</td>
<td align="left" width="63%">
Sets the wallpaper options.

</td>
</tr>
</table> 


## -remarks



Your code must include Wininet.h before it includes Shlobj.h. Failure to do so will result in a compiler error.




## -see-also




<a href="https://msdn.microsoft.com/68d72b0f-f5e9-4fff-bb13-4c60d1dd7009">Using the Active Desktop Object</a>
 

 


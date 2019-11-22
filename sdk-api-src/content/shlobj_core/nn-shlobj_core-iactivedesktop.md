---
UID: NN:shlobj_core.IActiveDesktop
title: IActiveDesktop (shlobj_core.h)

description: Allows a client program to manage the desktop items and wallpaper on a local computer.
old-location: lwef\iactivedesktop_interface.htm
tech.root: lwef
ms.assetid: 4d572b86-36e8-417b-857c-eb477c04c691

ms.date: 12/05/2018
ms.keywords: IActiveDesktop, IActiveDesktop interface [Legacy Windows Environment Features], IActiveDesktop interface [Legacy Windows Environment Features],described, _win32_IActiveDesktop_Interface, lwef.iactivedesktop_interface, shell.iactivedesktop_interface, shlobj_core/IActiveDesktop
ms.topic: interface
f1_keywords: 
 - "shlobj_core/IActiveDesktop"
dev_langs:
 - c++
req.header: shlobj_core.h
req.include-header: 
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
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IActiveDesktop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActiveDesktop interface


## -description


Allows a client program to manage the desktop items and wallpaper on a local computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveDesktop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActiveDesktop</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem">AddDesktopItem</a>
</td>
<td align="left" width="63%">
Adds a desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui">AddDesktopItemWithUI</a>
</td>
<td align="left" width="63%">
Adds a desktop item to the Active Desktop after  displaying user interfaces that confirm the addition of the desktop item, verifying security zone permissions, and asking if the user wants to create a subscription.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl">AddUrl</a>
</td>
<td align="left" width="63%">
Adds the desktop item associated with the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges">ApplyChanges</a>
</td>
<td align="left" width="63%">
Applies changes to the Active Desktop and saves them in the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-generatedesktopitemhtml">GenerateDesktopItemHtml</a>
</td>
<td align="left" width="63%">
Generates a generic HTML page containing the given desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem">GetDesktopItem</a>
</td>
<td align="left" width="63%">
Gets the specified desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitembyid">GetDesktopItemByID</a>
</td>
<td align="left" width="63%">
Gets the desktop item that matches the given identification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitembysource">GetDesktopItemBySource</a>
</td>
<td align="left" width="63%">
Gets a desktop item using its source URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount">GetDesktopItemCount</a>
</td>
<td align="left" width="63%">
Gets a count of the desktop items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemoptions">GetDesktopItemOptions</a>
</td>
<td align="left" width="63%">
Gets the options for the desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getpattern">GetPattern</a>
</td>
<td align="left" width="63%">
Gets the current pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getwallpaper">GetWallpaper</a>
</td>
<td align="left" width="63%">
Gets the current wallpaper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-getwallpaperoptions">GetWallpaperOptions</a>
</td>
<td align="left" width="63%">
Gets the wallpaper options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-modifydesktopitem">ModifyDesktopItem</a>
</td>
<td align="left" width="63%">
Modifies the desktop item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-removedesktopitem">RemoveDesktopItem</a>
</td>
<td align="left" width="63%">
Removes the specified desktop item from the desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-setdesktopitemoptions">SetDesktopItemOptions</a>
</td>
<td align="left" width="63%">
Sets the item's options.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-setpattern">SetPattern</a>
</td>
<td align="left" width="63%">
Sets the Active Desktop pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-setwallpaper">SetWallpaper</a>
</td>
<td align="left" width="63%">
Sets the wallpaper for the Active Desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iactivedesktop-setwallpaperoptions">SetWallpaperOptions</a>
</td>
<td align="left" width="63%">
Sets the wallpaper options.

</td>
</tr>
</table> 


## -remarks



Your code must include Wininet.h before it includes Shlobj.h. Failure to do so will result in a compiler error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/lwef/active-desktop-interface">Using the Active Desktop Object</a>
 

 


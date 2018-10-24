---
UID: NN:shlobj_core.IShellIconOverlayManager
title: IShellIconOverlayManager
author: windows-sdk-content
description: IShellIconOverlayManager may be altered or unavailable.
old-location: shell\IShellIconOverlayManager.htm
tech.root: shell
ms.assetid: 769c3b0b-ece4-4406-a76c-cabc37901351
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IShellIconOverlayManager, IShellIconOverlayManager interface [Windows Shell], IShellIconOverlayManager interface [Windows Shell],described, _win32_IShellIconOverlayManager, shell.IShellIconOverlayManager, shlobj_core/IShellIconOverlayManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellIconOverlayManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellIconOverlayManager interface


## -description


<p class="CCE_Message">[<b>IShellIconOverlayManager</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods that retrieve the icon overlay information, including the overlay index and the image index for an IShellFolder object. This interface iterates through all the icon overlay IDs and keeps the information in an array.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellIconOverlayManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellIconOverlayManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellIconOverlayManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dd918a4-64c7-4d7a-846c-0751e23c05a2">GetFileOverlayInfo</a>
</td>
<td align="left" width="63%">
Gets the index of the icon overlay or the icon image for the specified file with the specified attributes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/052e1648-359c-4202-a3ca-c5bd8a7e54e5">GetReservedOverlayInfo</a>
</td>
<td align="left" width="63%">
Gets the index of the icon overlay or the icon image for the specified file with the specified attributes from one of the reserved overlays.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd6003b5-551d-41cc-8ca6-13ab245ed6fd">LoadNonloadedOverlayIdentifiers</a>
</td>
<td align="left" width="63%">
Loads any registered overlay identifiers, or handlers, that are not currently loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7abbdd28-72b8-4a91-81db-6afc1242a086">OverlayIndexFromImageIndex</a>
</td>
<td align="left" width="63%">
Finds the index of an overlay image for the specified icon image. It can add an overlay if one is not found for the icon.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79b1e1c7-a008-4f68-88a2-379715167410">RefreshOverlayImages</a>
</td>
<td align="left" width="63%">
Refreshes the overlay cache, the image list, or both.

</td>
</tr>
</table> 


## -remarks



Icon overlays are small images placed at the lower-left corner of the icon that represents a Shell object in Windows Explorer or on the desktop. They are used to add some extra information to the object's normal icon. A commonly used icon overlay is the small arrow that indicates that a file or folder is actually a link. For more information, see <a href="https://msdn.microsoft.com/1a1d03ca-0922-41df-8cec-e74a16ed3bd6">IShellIconOverlay</a>.

This interface must be implemented by all icon overlay handlers.

This interface is not typically called by applications.




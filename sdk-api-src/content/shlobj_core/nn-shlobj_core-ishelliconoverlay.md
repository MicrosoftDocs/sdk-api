---
UID: NN:shlobj_core.IShellIconOverlay
title: IShellIconOverlay
author: windows-sdk-content
description: Exposes methods that are used by a namespace extension to specify icon overlays for the objects it contains.
old-location: shell\IShellIconOverlay.htm
tech.root: shell
ms.assetid: 1a1d03ca-0922-41df-8cec-e74a16ed3bd6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IShellIconOverlay, IShellIconOverlay interface [Windows Shell], IShellIconOverlay interface [Windows Shell],described, _win32_IShellIconOverlay, shell.IShellIconOverlay, shlobj_core/IShellIconOverlay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
 - IShellIconOverlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellIconOverlay interface


## -description


Exposes methods that are used by a namespace extension to specify icon overlays for the objects it contains.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellIconOverlay</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellIconOverlay</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellIconOverlay</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae7c55a1-8540-44d3-9793-2d6ac849ef60">GetOverlayIconIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the icon overlay in the system image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5bde311-8b5f-4a8b-9fff-5d062c650b95">GetOverlayIndex</a>
</td>
<td align="left" width="63%">
Gets the overlay index in the system image list.

</td>
</tr>
</table> 


## -remarks



Icon overlays are small images placed at the lower-left corner of the icon that represents a Shell object. They are typically used to add some extra information to the icon. A commonly used icon overlay is the small arrow that indicates that a file or folder icon represents a shortcut.

Icon overlays are part of the system image list. They have two identifiers. One is a one-based overlay index that identifies the overlay relative to other overlays in the image list. The other is an image index that identifies the actual image. These two indexes are equivalent to the values that you assign to the <i>iOverlay</i> and <i>iImage</i> parameters, respectively, when you add an icon overlay to a private image list with <a href="https://msdn.microsoft.com/8cb1babc-01bd-4aae-9bc7-073050242ce4">ImageList::SetOverlayImage</a>.

Before displaying the icon for an object, the Shell calls the associated folder's <b>IShellIconOverlay</b> interface to query whether the object's icon should have an overlay. Typically it calls <a href="https://msdn.microsoft.com/e5bde311-8b5f-4a8b-9fff-5d062c650b95">IShellIconOverlay::GetOverlayIndex</a> to request the overlay's overlay index. In some cases, the Shell might call <a href="https://msdn.microsoft.com/ae7c55a1-8540-44d3-9793-2d6ac849ef60">IShellIconOverlay::GetOverlayIconIndex</a> to request the overlay's image index. To specify an icon overlay, the methods must return the requested index. Otherwise, they return S_FALSE.

To specify an icon overlay, both methods must first retrieve the overlay's overlay index in the system image list by calling <a href="https://msdn.microsoft.com/20001ae0-05d0-46a7-8bb8-9bb722f5d795">SHGetIconOverlayIndex</a>. When <b>SHGetIconOverlayIndex</b> is called for the first time, the Shell uses the overlay's file name and index within the file to add the image to the system image list. Once an overlay is in the system image list, the Shell simply uses the file name and index as an identifier. You can also use <b>SHGetIconOverlayIndex</b> to retrieve the overlay index of several standard system overlays. <a href="https://msdn.microsoft.com/e5bde311-8b5f-4a8b-9fff-5d062c650b95">IShellIconOverlay::GetOverlayIndex</a> simply returns the overlay index to the Shell. <a href="https://msdn.microsoft.com/ae7c55a1-8540-44d3-9793-2d6ac849ef60">IShellIconOverlay::GetOverlayIconIndex</a> must use the <a href="https://msdn.microsoft.com/6619d390-0c23-41ff-a07b-31425e47712b">INDEXTOOVERLAYMASK</a> macro to convert the overlay index to the equivalent image index.

 The number of different icon overlay handlers that the system can support is limited by the amount of space available for icon overlays in the system image list. There are currently fifteen slots allotted for icon overlays, some of which are reserved by the system. For this reason, icon overlays should be specified only if there are no satisfactory alternatives.

This interface is implemented by namespace extensions that need to specify icon overlays for their objects.

This interface is not typically used by applications.




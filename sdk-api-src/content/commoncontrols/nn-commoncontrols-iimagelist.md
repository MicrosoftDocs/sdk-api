---
UID: NN:commoncontrols.IImageList
title: IImageList
author: windows-sdk-content
description: Exposes methods that manipulate and interact with image lists.
old-location: controls\IImageList.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\iimagelist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IImageList, IImageList interface [Windows Controls], IImageList interface [Windows Controls],described, comctl_IImageList, comctl_IImageList_cpp, commoncontrols/IImageList, controls.IImageList, controls.comctl_IImageList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: commoncontrols.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CommonControls.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OFNOTIFYW, *LPOFNOTIFYW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comctl32.dll
api_name:
 - IImageList
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
---

# IImageList interface


## -description


Exposes methods that manipulate and interact with image lists.

            
        

To use <b>IImageList</b>, specify Comctl32.dll version 6 in the manifest. If you do not do this, Comctl32.dll version 5 will be used by default, with which <b>IImageList</b> could display unpredictable behavior. For more information on manifests, see <a href="https://msdn.microsoft.com/en-us/library/Bb773175(v=VS.85).aspx">Enabling Visual Styles</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImageList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IImageList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImageList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an image or images to an image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761438(v=VS.85).aspx">AddMasked</a>
</td>
<td align="left" width="63%">
Adds an image or images to an image list, generating a mask from the specified bitmap. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761440(v=VS.85).aspx">BeginDrag</a>
</td>
<td align="left" width="63%">
Begins dragging an image.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Clones an existing image list.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff544217">Copy</a>
</td>
<td align="left" width="63%">
Copies images from a given image list.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761446(v=VS.85).aspx">DragEnter</a>
</td>
<td align="left" width="63%">
Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761448(v=VS.85).aspx">DragLeave</a>
</td>
<td align="left" width="63%">
Unlocks the specified window and hides the drag image, which enables the window to update.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761451(v=VS.85).aspx">DragMove</a>
</td>
<td align="left" width="63%">
Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a <a href="https://msdn.microsoft.com/en-us/library/ms645616(v=VS.85).aspx">WM_MOUSEMOVE</a> message.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761453(v=VS.85).aspx">DragShowNolock</a>
</td>
<td align="left" width="63%">
Shows or hides the image being dragged. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761455(v=VS.85).aspx">Draw</a>
</td>
<td align="left" width="63%">
Draws an image list item in the specified device context.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761457(v=VS.85).aspx">EndDrag</a>
</td>
<td align="left" width="63%">
Ends a drag operation. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761459(v=VS.85).aspx">GetBkColor</a>
</td>
<td align="left" width="63%">
Gets the current background color for an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761461(v=VS.85).aspx">GetDragImage</a>
</td>
<td align="left" width="63%">
Gets the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761463(v=VS.85).aspx">GetIcon</a>
</td>
<td align="left" width="63%">
Creates an icon from an image and a mask in an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761478(v=VS.85).aspx">GetIconSize</a>
</td>
<td align="left" width="63%">
Gets the dimensions of images in an image list. All images in an image list have the same dimensions. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761480(v=VS.85).aspx">GetImageCount</a>
</td>
<td align="left" width="63%">
Gets the number of images in an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761482(v=VS.85).aspx">GetImageInfo</a>
</td>
<td align="left" width="63%">
Gets information about an image. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761484(v=VS.85).aspx">GetImageRect</a>
</td>
<td align="left" width="63%">
Gets an image's bounding rectangle.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761486(v=VS.85).aspx">GetItemFlags</a>
</td>
<td align="left" width="63%">
Gets the flags of an image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761488(v=VS.85).aspx">GetOverlayImage</a>
</td>
<td align="left" width="63%">
Retrieves a specified image from the list of images used as overlay masks. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926900">Merge</a>
</td>
<td align="left" width="63%">
Creates a new image by combining two existing images. This method also creates a new image list in which to store the image. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an image from an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761496(v=VS.85).aspx">Replace</a>
</td>
<td align="left" width="63%">
Replaces an image in an image list with a new image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761498(v=VS.85).aspx">ReplaceIcon</a>
</td>
<td align="left" width="63%">
Replaces an image with an icon or cursor. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761500(v=VS.85).aspx">SetBkColor</a>
</td>
<td align="left" width="63%">
Sets the background color for an image list. This method only functions if you add an icon to the image list or use the <a href="https://msdn.microsoft.com/en-us/library/Bb761438(v=VS.85).aspx">IImageList::AddMasked</a> method to add a black and white bitmap. Without a mask, the entire image draws, and the background color is not visible. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761502(v=VS.85).aspx">SetDragCursorImage</a>
</td>
<td align="left" width="63%">
Creates a new drag image by combining the specified image, which is typically a mouse cursor image, with the current drag image. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761504(v=VS.85).aspx">SetIconSize</a>
</td>
<td align="left" width="63%">
Sets the dimensions of images in an image list and removes all images from the list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761506(v=VS.85).aspx">SetImageCount</a>
</td>
<td align="left" width="63%">
Resizes an existing image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb761508(v=VS.85).aspx">SetOverlayImage</a>
</td>
<td align="left" width="63%">
Adds a specified image to the list of images used as overlay masks. An image list can have up to four overlay masks in Common Controls <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">version 4.70</a> and earlier, and up to 15 in version 4.71 or later. The method assigns an overlay mask index to the specified image. 
		

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761389(v=VS.85).aspx">Image Lists</a>
 

 


---
UID: NN:commoncontrols.IImageList
title: IImageList
author: windows-sdk-content
description: Exposes methods that manipulate and interact with image lists.
old-location: controls\IImageList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\ifaces\iimagelist\iimagelist.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
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
req.lib: 
req.dll: Comctl32.dll (version 6.0 or later)
req.irql: 
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
req.typenames: 
req.redist: 
---

# IImageList interface


## -description


Exposes methods that manipulate and interact with image lists.

            
        

To use <b>IImageList</b>, specify Comctl32.dll version 6 in the manifest. If you do not do this, Comctl32.dll version 5 will be used by default, with which <b>IImageList</b> could display unpredictable behavior. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.


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
<a href="https://msdn.microsoft.com/1dafbf09-6ac7-440b-a005-a6fe1dca4c17">Add</a>
</td>
<td align="left" width="63%">
Adds an image or images to an image list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4953332-e351-4f75-a128-bed98ab9adb4">AddMasked</a>
</td>
<td align="left" width="63%">
Adds an image or images to an image list, generating a mask from the specified bitmap. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/403fede8-7b13-470d-9200-f3cc831d3132">BeginDrag</a>
</td>
<td align="left" width="63%">
Begins dragging an image.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0ad7e66-2d42-443c-9f0d-9235b1d5d823">Clone</a>
</td>
<td align="left" width="63%">
Clones an existing image list.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d1bdb15-8cb4-4a8b-8a4c-eaadd03b5ace">Copy</a>
</td>
<td align="left" width="63%">
Copies images from a given image list.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b33886e3-1305-4876-b5a9-56a849c267c7">DragEnter</a>
</td>
<td align="left" width="63%">
Locks updates to the specified window during a drag operation and displays the drag image at the specified position within the window. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b88edf69-b505-4320-be1c-db64d71d7a72">DragLeave</a>
</td>
<td align="left" width="63%">
Unlocks the specified window and hides the drag image, which enables the window to update.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92d020d5-b2e0-4778-b379-d2029062a5f0">DragMove</a>
</td>
<td align="left" width="63%">
Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> message.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca4384f6-70e0-4231-890d-f2bf03db3d4a">DragShowNolock</a>
</td>
<td align="left" width="63%">
Shows or hides the image being dragged. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a52a225-b5b3-444d-8878-a8d6de7478ee">Draw</a>
</td>
<td align="left" width="63%">
Draws an image list item in the specified device context.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27306f01-0c5d-4bf2-8b25-180617ee0e3a">EndDrag</a>
</td>
<td align="left" width="63%">
Ends a drag operation. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2829e921-86b2-4106-8261-36dbfec0298e">GetBkColor</a>
</td>
<td align="left" width="63%">
Gets the current background color for an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cf57bb7-8344-4b9c-9377-c22823a2f4df">GetDragImage</a>
</td>
<td align="left" width="63%">
Gets the temporary image list that is used for the drag image. The function also retrieves the current drag position and the offset of the drag image relative to the drag position. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be53ccf2-bc96-48cc-a0ac-2a8a6c3abdef">GetIcon</a>
</td>
<td align="left" width="63%">
Creates an icon from an image and a mask in an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fa4ed4c-2825-4da0-8944-9951b05e8889">GetIconSize</a>
</td>
<td align="left" width="63%">
Gets the dimensions of images in an image list. All images in an image list have the same dimensions. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63005fd3-092d-4063-863e-0cbb0dc65923">GetImageCount</a>
</td>
<td align="left" width="63%">
Gets the number of images in an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a08fbc4d-96f0-403d-8062-0592ab32dc5c">GetImageInfo</a>
</td>
<td align="left" width="63%">
Gets information about an image. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de0a5aac-5ae4-4169-a044-e7184cf2a4f3">GetImageRect</a>
</td>
<td align="left" width="63%">
Gets an image's bounding rectangle.
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/508b808b-409f-49f7-9a7a-c98f6d9781da">GetItemFlags</a>
</td>
<td align="left" width="63%">
Gets the flags of an image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a3623e0-7333-4cd8-b138-f1c3c1437586">GetOverlayImage</a>
</td>
<td align="left" width="63%">
Retrieves a specified image from the list of images used as overlay masks. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f72fae4-3111-409e-967f-2b73336f772b">Merge</a>
</td>
<td align="left" width="63%">
Creates a new image by combining two existing images. This method also creates a new image list in which to store the image. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96d20b2c-78d6-424c-a45a-58b68070286d">Remove</a>
</td>
<td align="left" width="63%">
Removes an image from an image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a8cd814-2b48-4ab4-9d7b-24c049c8e8fc">Replace</a>
</td>
<td align="left" width="63%">
Replaces an image in an image list with a new image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef0ba268-da09-466d-b62f-59cee970dc4e">ReplaceIcon</a>
</td>
<td align="left" width="63%">
Replaces an image with an icon or cursor. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81f0ccf3-c2e9-438d-9326-74fadea62c7b">SetBkColor</a>
</td>
<td align="left" width="63%">
Sets the background color for an image list. This method only functions if you add an icon to the image list or use the <a href="https://msdn.microsoft.com/e4953332-e351-4f75-a128-bed98ab9adb4">IImageList::AddMasked</a> method to add a black and white bitmap. Without a mask, the entire image draws, and the background color is not visible. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/118e2c93-de47-429e-a7dc-a0db939d7851">SetDragCursorImage</a>
</td>
<td align="left" width="63%">
Creates a new drag image by combining the specified image, which is typically a mouse cursor image, with the current drag image. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cf63e11-6e03-4b8d-a2db-2764ec2cd9bf">SetIconSize</a>
</td>
<td align="left" width="63%">
Sets the dimensions of images in an image list and removes all images from the list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bf63c67-7a0e-4d5e-8618-4de5e4b31836">SetImageCount</a>
</td>
<td align="left" width="63%">
Resizes an existing image list. 
		

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30f2a85b-7109-4cf7-b047-0dbd330e1d8d">SetOverlayImage</a>
</td>
<td align="left" width="63%">
Adds a specified image to the list of images used as overlay masks. An image list can have up to four overlay masks in Common Controls <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">version 4.70</a> and earlier, and up to 15 in version 4.71 or later. The method assigns an overlay mask index to the specified image. 
		

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/01a96f65-51eb-489f-b6e4-234309f2077b">Image Lists</a>
 

 


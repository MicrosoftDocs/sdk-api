---
UID: NN:shlobj_core.IShellFolderView
title: IShellFolderView
author: windows-sdk-content
description: Exposes methods that manipulate Shell folder views.
old-location: shell\IShellFolderView.htm
tech.root: Shell
ms.assetid: e3b0b35f-6707-4e37-8470-31b1d4421d07
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IShellFolderView, IShellFolderView interface [Windows Shell], IShellFolderView interface [Windows Shell],described, _shell_IShellFolderView, shell.IShellFolderView, shlobj_core/IShellFolderView
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shlobj_core.h
api_name:
 - IShellFolderView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellFolderView interface


## -description


<p class="CCE_Message">[<b>IShellFolderView</b> is no longer available for use as of Windows 7. Instead, use <a href="https://msdn.microsoft.com/52fcf0df-f532-4114-b1c9-96838f1a5e77">IFolderView2</a> and <a href="https://msdn.microsoft.com/3bc2615e-f07c-4959-b89e-bbbd2bf45a94">IFolderView</a>.]

Exposes methods that manipulate Shell folder views.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellFolderView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50f07c12-7c66-40a0-b710-a4240fde859a">AddObject</a>
</td>
<td align="left" width="63%">
Adds an item to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cb77a02-82da-42d3-97a3-ff47a9ce1831">ArrangeGrid</a>
</td>
<td align="left" width="63%">
Arranges moved icons so that they align to an invisible grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37260573-bac0-462c-a0df-654e2b22ed47">AutoArrange</a>
</td>
<td align="left" width="63%">
Arranges moved icons so that they tend toward the left side of the viewing area and displace other icons with which they come into contact.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15eda2f2-6956-47c1-be08-3ca2f292578e">GetArrangeParam</a>
</td>
<td align="left" width="63%">
Gets the arrangement parameter of the view, which is how the view has been sorted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee7c0c7c-17f1-48b4-9aa0-33804c237036">GetAutoArrange</a>
</td>
<td align="left" width="63%">
Gets the current state of the folder's Auto Arrange mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ea29e97-41cb-4de7-8320-1d6389cfb6f6">GetDragPoint</a>
</td>
<td align="left" width="63%">
Gets the point at which the current drag-and-drop operation was initiated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ea09e0f-adf0-4d33-a7c7-c8a4aa6b30ea">GetDropPoint</a>
</td>
<td align="left" width="63%">
Gets the point at which the current drag-and-drop operation was terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92450bc7-26e5-4061-90f7-eea0f0a4db09">GetItemSpacing</a>
</td>
<td align="left" width="63%">
Gets the spacing for small and large view modes only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a231e92f-b467-4fd7-929d-92259272a734">GetObject</a>
</td>
<td align="left" width="63%">
Gets an item from the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a68dca56-ae89-4280-b1de-8c85362bf9c6">GetObjectCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d504eba-7fb8-44a0-9534-4e7995b9b5d4">GetSelectedCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the view that are selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cb41312-a401-4d24-a7a7-7b03478cf684">GetSelectedObjects</a>
</td>
<td align="left" width="63%">
Gets an array of the objects in the view that are selected and the number of those objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6de58057-2bcd-480e-8b4a-6e59aad168dc">IsBkDropTarget</a>
</td>
<td align="left" width="63%">
Checks if the target of a drag-and-drop operation is the background of the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3661fe68-b351-48e0-a098-8ad919bdfbb2">IsDropOnSource</a>
</td>
<td align="left" width="63%">
Checks whether the destination of the current drag-and-drop or cut-and-paste operation is the same as the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/294fbafc-6a8f-4617-bc34-413c89e3a43c">MoveIcons</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e998e31-7842-4d17-a9e6-35663ff1474a">QuerySupport</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fe955db-dab3-4e53-9c1b-979794052035">Rearrange</a>
</td>
<td align="left" width="63%">
Rearranges the items in a view according to a sorting rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6165d2d1-4bd6-4a18-8191-1fd7e924d7d8">RefreshObject</a>
</td>
<td align="left" width="63%">
Redraws the given item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e96040b-5b6a-4323-a5c4-f30e534ed15a">RemoveObject</a>
</td>
<td align="left" width="63%">
Removes an item from the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80ec6587-515f-4697-8a19-8c486bec3473">Select</a>
</td>
<td align="left" width="63%">
Selects and/or unselects items in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/742b0d93-5cdf-4498-80c2-2d33359f146f">SetAutomationObject</a>
</td>
<td align="left" width="63%">
Replaces the internal automation object of the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3438f4ba-e7f1-46b1-b85d-0e880615bb12">SetCallback</a>
</td>
<td align="left" width="63%">
Replaces the <a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a> that <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/372cc6db-f9c1-4110-98aa-a7ad90312048">SetClipboard</a>
</td>
<td align="left" width="63%">
Performs a cut operation on the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d905260c-fa68-4b39-9c94-a74e1ac71b95">SetItemPos</a>
</td>
<td align="left" width="63%">
Sets the position of the given item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0656fb51-1d10-42a5-bd4a-3ceb606c7176">SetObjectCount</a>
</td>
<td align="left" width="63%">
Sets the number of items in the ListView control that the view contains.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a226139a-c2b0-44d5-a0c3-790e27ab3a0f">SetPoints</a>
</td>
<td align="left" width="63%">
Copies the points at which the current selection is located into a data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe249faa-561f-4179-a478-4ff284ffa963">SetRedraw</a>
</td>
<td align="left" width="63%">
Allows a view to be redrawn or prevents it from being redrawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aacc326f-30e3-4794-b158-77ccf24f8d01">UpdateObject</a>
</td>
<td align="left" width="63%">
Replaces an item in a view with another item.

</td>
</tr>
</table> 


## -remarks



<b>IShellFolderView</b> is supported by the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> object that is returned from <a href="https://msdn.microsoft.com/7edd6786-7d74-4065-8cf1-cbb489007a46">SHCreateShellFolderViewEx</a>.  This object contains a ListView control and some of the methods on <b>IShellFolderView</b> directly manipulate this ListView control.




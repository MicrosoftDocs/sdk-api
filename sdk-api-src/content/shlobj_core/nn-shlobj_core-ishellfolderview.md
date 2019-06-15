---
UID: NN:shlobj_core.IShellFolderView
title: IShellFolderView (shlobj_core.h)
author: windows-sdk-content
description: Exposes methods that manipulate Shell folder views.
old-location: shell\IShellFolderView.htm
tech.root: shell
ms.assetid: e3b0b35f-6707-4e37-8470-31b1d4421d07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellFolderView, IShellFolderView interface [Windows Shell], IShellFolderView interface [Windows Shell],described, _shell_IShellFolderView, shell.IShellFolderView, shlobj_core/IShellFolderView
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
ms.custom: 19H1
---

# IShellFolderView interface


## -description


<p class="CCE_Message">[<b>IShellFolderView</b> is no longer available for use as of Windows 7. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2">IFolderView2</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>.]

Exposes methods that manipulate Shell folder views.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderView</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellFolderView</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-addobject">AddObject</a>
</td>
<td align="left" width="63%">
Adds an item to the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-arrangegrid">ArrangeGrid</a>
</td>
<td align="left" width="63%">
Arranges moved icons so that they align to an invisible grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-autoarrange">AutoArrange</a>
</td>
<td align="left" width="63%">
Arranges moved icons so that they tend toward the left side of the viewing area and displace other icons with which they come into contact.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getarrangeparam">GetArrangeParam</a>
</td>
<td align="left" width="63%">
Gets the arrangement parameter of the view, which is how the view has been sorted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getautoarrange">GetAutoArrange</a>
</td>
<td align="left" width="63%">
Gets the current state of the folder's Auto Arrange mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getdragpoint">GetDragPoint</a>
</td>
<td align="left" width="63%">
Gets the point at which the current drag-and-drop operation was initiated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getdroppoint">GetDropPoint</a>
</td>
<td align="left" width="63%">
Gets the point at which the current drag-and-drop operation was terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing">GetItemSpacing</a>
</td>
<td align="left" width="63%">
Gets the spacing for small and large view modes only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Gets an item from the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getobjectcount">GetObjectCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the folder view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getselectedcount">GetSelectedCount</a>
</td>
<td align="left" width="63%">
Gets the number of items in the view that are selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getselectedobjects">GetSelectedObjects</a>
</td>
<td align="left" width="63%">
Gets an array of the objects in the view that are selected and the number of those objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-isbkdroptarget">IsBkDropTarget</a>
</td>
<td align="left" width="63%">
Checks if the target of a drag-and-drop operation is the background of the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-isdroponsource">IsDropOnSource</a>
</td>
<td align="left" width="63%">
Checks whether the destination of the current drag-and-drop or cut-and-paste operation is the same as the source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-moveicons">MoveIcons</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-querysupport">QuerySupport</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-rearrange">Rearrange</a>
</td>
<td align="left" width="63%">
Rearranges the items in a view according to a sorting rule.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-refreshobject">RefreshObject</a>
</td>
<td align="left" width="63%">
Redraws the given item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-removeobject">RemoveObject</a>
</td>
<td align="left" width="63%">
Removes an item from the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-select">Select</a>
</td>
<td align="left" width="63%">
Selects and/or unselects items in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-setautomationobject">SetAutomationObject</a>
</td>
<td align="left" width="63%">
Replaces the internal automation object of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-setcallback">SetCallback</a>
</td>
<td align="left" width="63%">
Replaces the <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb">IShellFolderViewCB</a> that <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-setclipboard">SetClipboard</a>
</td>
<td align="left" width="63%">
Performs a cut operation on the current selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-setitempos">SetItemPos</a>
</td>
<td align="left" width="63%">
Sets the position of the given item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-setobjectcount">SetObjectCount</a>
</td>
<td align="left" width="63%">
Sets the number of items in the ListView control that the view contains.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-setpoints">SetPoints</a>
</td>
<td align="left" width="63%">
Copies the points at which the current selection is located into a data object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-setredraw">SetRedraw</a>
</td>
<td align="left" width="63%">
Allows a view to be redrawn or prevents it from being redrawn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-updateobject">UpdateObject</a>
</td>
<td align="left" width="63%">
Replaces an item in a view with another item.

</td>
</tr>
</table> 


## -remarks



<b>IShellFolderView</b> is supported by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> object that is returned from <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>.  This object contains a ListView control and some of the methods on <b>IShellFolderView</b> directly manipulate this ListView control.




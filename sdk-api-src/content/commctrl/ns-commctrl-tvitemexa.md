---
UID: NS:commctrl.tagTVITEMEXA
title: TVITEMEXA (commctrl.h)
description: Specifies or receives attributes of a tree-view item. This structure is an enhancement to the TVITEM structure. New applications should use this structure where appropriate. (ANSI)
helpviewer_keywords: ["*LPTVITEMEXA","I_CHILDRENAUTO","I_CHILDRENCALLBACK","LPTVITEMEX","LPTVITEMEX structure pointer [Windows Controls]","TVIF_CHILDREN","TVIF_DI_SETITEM","TVIF_EXPANDEDIMAGE","TVIF_HANDLE","TVIF_IMAGE","TVIF_INTEGRAL","TVIF_PARAM","TVIF_SELECTEDIMAGE","TVIF_STATE","TVIF_STATEEX","TVIF_TEXT","TVIS_EX_DISABLED","TVIS_EX_FLAT","TVIS_EX_HWND","TVITEMEX","TVITEMEX structure [Windows Controls]","TVITEMEXA","TVITEMEXW","_win32_TVITEMEX","_win32_TVITEMEX_cpp","commctrl/LPTVITEMEX","commctrl/TVITEMEX","commctrl/TVITEMEXA","commctrl/TVITEMEXW","controls.TVITEMEX","controls._win32_TVITEMEX","one","zero"]
old-location: controls\TVITEMEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\tvitemex.htm
ms.date: 12/05/2018
ms.keywords: '*LPTVITEMEXA, I_CHILDRENAUTO, I_CHILDRENCALLBACK, LPTVITEMEX, LPTVITEMEX structure pointer [Windows Controls], TVIF_CHILDREN, TVIF_DI_SETITEM, TVIF_EXPANDEDIMAGE, TVIF_HANDLE, TVIF_IMAGE, TVIF_INTEGRAL, TVIF_PARAM, TVIF_SELECTEDIMAGE, TVIF_STATE, TVIF_STATEEX, TVIF_TEXT, TVIS_EX_DISABLED, TVIS_EX_FLAT, TVIS_EX_HWND, TVITEMEX, TVITEMEX structure [Windows Controls], TVITEMEXA, TVITEMEXW, _win32_TVITEMEX, _win32_TVITEMEX_cpp, commctrl/LPTVITEMEX, commctrl/TVITEMEX, commctrl/TVITEMEXA, commctrl/TVITEMEXW, controls.TVITEMEX, controls._win32_TVITEMEX, one, zero'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TVITEMEXW (Unicode) and TVITEMEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TVITEMEXA, *LPTVITEMEXA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTVITEMEXA
 - commctrl/tagTVITEMEXA
 - LPTVITEMEXA
 - commctrl/LPTVITEMEXA
 - TVITEMEXA
 - commctrl/TVITEMEXA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TVITEMEX
 - TVITEMEXA
 - TVITEMEXW
---

# TVITEMEXA structure


## -description

Specifies or receives attributes of a tree-view item. This structure is an enhancement to the <a href="/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> structure. New applications should use this structure where appropriate.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Array of flags that indicate which of the other structure members contain valid data. When this structure is used with the <a href="/windows/desktop/Controls/tvm-getitem">TVM_GETITEM</a> message, the <b>mask</b> member indicates the item attributes to retrieve. If used with the <a href="/windows/desktop/Controls/tvm-setitem">TVM_SETITEM</a> message, the <b>mask</b> indicates the attributes to set. This member can be one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVIF_CHILDREN"></a><a id="tvif_children"></a><dl>
<dt><b>TVIF_CHILDREN</b></dt>
</dl>
</td>
<td width="60%">
The <b>cChildren</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_DI_SETITEM"></a><a id="tvif_di_setitem"></a><dl>
<dt><b>TVIF_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">
The tree-view control will retain the supplied information and will not request it again. This flag is valid only when processing the <a href="/windows/desktop/Controls/tvn-getdispinfo">TVN_GETDISPINFO</a> notification.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_EXPANDEDIMAGE"></a><a id="tvif_expandedimage"></a><dl>
<dt><b>TVIF_EXPANDEDIMAGE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b> The <b>iExpandedImage</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_HANDLE"></a><a id="tvif_handle"></a><dl>
<dt><b>TVIF_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>hItem</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_IMAGE"></a><a id="tvif_image"></a><dl>
<dt><b>TVIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iImage</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_INTEGRAL"></a><a id="tvif_integral"></a><dl>
<dt><b>TVIF_INTEGRAL</b></dt>
</dl>
</td>
<td width="60%">
The <b>iIntegral</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_PARAM"></a><a id="tvif_param"></a><dl>
<dt><b>TVIF_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The <b>lParam</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_SELECTEDIMAGE"></a><a id="tvif_selectedimage"></a><dl>
<dt><b>TVIF_SELECTEDIMAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iSelectedImage</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_STATE"></a><a id="tvif_state"></a><dl>
<dt><b>TVIF_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>state</b> and <b>stateMask</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_STATEEX"></a><a id="tvif_stateex"></a><dl>
<dt><b>TVIF_STATEEX</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b> The <b>uStateEx</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIF_TEXT"></a><a id="tvif_text"></a><dl>
<dt><b>TVIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszText</b> and <b>cchTextMax</b> members are valid.

</td>
</tr>
</table>

### -field hItem

Type: <b>HTREEITEM</b>

Handle to the item.

### -field state

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Set of bit flags and image list indexes that indicate the item's state. When setting the state of an item, the <b>stateMask</b> member indicates the valid bits of this member. When retrieving the state of an item, this member returns the current state for the bits indicated in the <b>stateMask</b> member.
For more information regarding this member, see remarks section.

                    

Bits 0 through 7 of this member contain the item state flags. For a list of possible item state flags, see <a href="/windows/desktop/Controls/tree-view-control-item-states">Tree-View Control Item States</a>.

Bits 8 through 11 of this member specify the one-based overlay image index. The overlay image is superimposed over the item's icon image. If these bits are zero, the item has no overlay image. To isolate these bits, use the <a href="/windows/desktop/Controls/tree-view-control-item-states">TVIS_OVERLAYMASK</a> mask. To set the overlay image index in this member, use the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a> macro. The image list's overlay images are set with the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_setoverlayimage">ImageList_SetOverlayImage</a> function.

A state image is displayed next to an item's icon to indicate an application-defined state. Specify the state image list by sending a <a href="/windows/desktop/Controls/tvm-setimagelist">TVM_SETIMAGELIST</a> message. To set an item's state image, include the <a href="/windows/desktop/Controls/tree-view-control-item-states">TVIS_STATEIMAGEMASK</a> value in The <b>stateMask</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-tvitema">TVITEM</a> structure. Bits 12 through 15 of the structure's
<b>state</b> member specify the index in the state image list of the image to be drawn.

To set the state image index, use <a href="/windows/desktop/api/commctrl/nf-commctrl-indextostateimagemask">INDEXTOSTATEIMAGEMASK</a>. This macro takes an index and sets bits 12 through 15 appropriately. To indicate that the item has no state image, set the index to zero. This convention means that image zero in the state image list cannot be used as a state image. To isolate bits 12 through 15 of The <b>state</b> member, use the <a href="/windows/desktop/Controls/tree-view-control-item-states">TVIS_STATEIMAGEMASK</a> mask.

### -field stateMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Bits of the <b>state</b> member that are valid. If you are retrieving an item's state, set the bits of the <b>stateMask</b> member to indicate the bits to be returned in the <b>state</b> member. If you are setting an item's state, set the bits of the <b>stateMask</b> member to indicate the bits of the <b>state</b> member that you want to set. To set or retrieve an item's overlay image index, set the <a href="/windows/desktop/Controls/tree-view-control-item-states">TVIS_OVERLAYMASK</a> bits. To set or retrieve an item's state image index, set the <a href="/windows/desktop/Controls/tree-view-control-item-states">TVIS_STATEIMAGEMASK</a> bits.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to a null-terminated string that contains the item text if the structure specifies item attributes. If this member is the LPSTR_TEXTCALLBACK value, the parent window is responsible for storing the name. In this case, the tree-view control sends the parent window a <a href="/windows/desktop/Controls/tvn-getdispinfo">TVN_GETDISPINFO</a> notification code when it needs the item text for displaying, sorting, or editing and a <a href="/windows/desktop/Controls/tvn-setdispinfo">TVN_SETDISPINFO</a> notification code when the item text changes. If the structure is receiving item attributes, this member is the address of the buffer that receives the item text. Note that although the tree-view control allows any length string to be stored as item text, only the first 260 characters are displayed.

### -field cchTextMax

Type: <b>int</b>

Size of the buffer pointed to by the <b>pszText</b> member, in characters. If this structure is being used to set item attributes, this member is ignored.

### -field iImage

Type: <b>int</b>

Index in the tree-view control's image list of the icon image to use when the item is in the nonselected state. If this member is the I_IMAGECALLBACK value, the parent window is responsible for storing the index. In this case, the tree-view control sends the parent a <a href="/windows/desktop/Controls/tvn-getdispinfo">TVN_GETDISPINFO</a> notification code to retrieve the index when it needs to display the image.

### -field iSelectedImage

Type: <b>int</b>

Index in the tree-view control's image list of the icon image to use when the item is in the selected state. If this member is the I_IMAGECALLBACK value, the parent window is responsible for storing the index. In this case, the tree-view control sends the parent a <a href="/windows/desktop/Controls/tvn-getdispinfo">TVN_GETDISPINFO</a> notification code to retrieve the index when it needs to display the image.

### -field cChildren

Type: <b>int</b>

Flag that indicates whether the item has associated child items. This member can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>zero</b></dt>
</dl>
</td>
<td width="60%">
The item has no child items.

</td>
</tr>
<tr>
<td width="40%"><a id="one"></a><a id="ONE"></a><dl>
<dt><b>one</b></dt>
</dl>
</td>
<td width="60%">
The item has one or more child items.

</td>
</tr>
<tr>
<td width="40%"><a id="I_CHILDRENCALLBACK"></a><a id="i_childrencallback"></a><dl>
<dt><b>I_CHILDRENCALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The parent window keeps track of whether the item has child items. In this case, when the tree-view control needs to display the item, the control sends the parent a <a href="/windows/desktop/Controls/tvn-getdispinfo">TVN_GETDISPINFO</a> notification code to determine whether the item has child items. If the tree-view control has the <a href="/windows/desktop/Controls/tree-view-control-window-styles">TVS_HASBUTTONS</a> style, it uses this member to determine whether to display the button indicating the presence of child items. You can use this member to force the control to display the button even though the item does not have any child items inserted. This allows you to display the button while minimizing the control's memory usage by inserting child items only when the item is visible or expanded.

</td>
</tr>
<tr>
<td width="40%"><a id="I_CHILDRENAUTO"></a><a id="i_childrenauto"></a><dl>
<dt><b>I_CHILDRENAUTO</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.0</a> <b>Intended for internal use; not recommended for use in applications.</b> The tree-view control automatically determines whether the item has child items. 


<div class="alert"><b>Note</b>  This flag may not be supported in future versions of Comctl32.dll. Also, this flag is not defined in commctrl.h. Add the following definition to the source files of your application to use the flag: 

```
#define I_CHILDRENAUTO (-2)
```


</div>
<div> </div>
</td>
</tr>
</table>

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

A value to associate with the item.

### -field iIntegral

Type: <b>int</b>

Height of the item, in multiples of the standard item height (see <a href="/windows/desktop/Controls/tvm-setitemheight">TVM_SETITEMHEIGHT</a>). For example, setting this member to 2 will give the item twice the standard height. The tree-view control does not draw in the extra area, which appears below the item content, but this space can be used by the application for drawing when using <a href="/windows/desktop/Controls/custom-draw">custom draw</a>. Applications that are not using custom draw should set this value to 1, as otherwise the behavior is undefined.

### -field uStateEx

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

<b>Internet Explorer 6 and later</b>. One or more (as a bitwise combination) of the following extended states.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVIS_EX_DISABLED"></a><a id="tvis_ex_disabled"></a><dl>
<dt><b>TVIS_EX_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later</b>. Creates a control that is drawn in gray, that the user cannot interact with.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIS_EX_FLAT"></a><a id="tvis_ex_flat"></a><dl>
<dt><b>TVIS_EX_FLAT</b></dt>
</dl>
</td>
<td width="60%">
Creates a flat item—the item is virtual and is not visible in the tree; instead, its children take its place in the tree hierarchy. This state is valid only when adding an item to the tree-view control.

</td>
</tr>
<tr>
<td width="40%"><a id="TVIS_EX_HWND"></a><a id="tvis_ex_hwnd"></a><dl>
<dt><b>TVIS_EX_HWND</b></dt>
</dl>
</td>
<td width="60%">
Creates a separate HWND for the item. This state is valid only when adding an item to the tree-view control.

</td>
</tr>
</table>

### -field hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

<b>Internet Explorer 6 and later</b>. Not used; must be <b>NULL</b>.

### -field iExpandedImage

Type: <b>int</b>

<b>Internet Explorer 6 and later</b>. Index of the image in the control's image list to display when the item is in the expanded state.

### -field iReserved

Type: <b>int</b>

Reserved member. Do not use.

## -see-also

<a href="/windows/desktop/Controls/using-treeview">Adding Tree-View Items</a>

## -remarks

> [!NOTE]
> The commctrl.h header defines TVITEMEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

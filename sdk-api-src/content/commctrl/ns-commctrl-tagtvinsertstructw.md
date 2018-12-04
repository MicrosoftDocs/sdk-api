---
UID: NS:commctrl.tagTVINSERTSTRUCTW
title: tagTVINSERTSTRUCTW
author: windows-sdk-content
description: Contains information used to add a new item to a tree-view control. This structure is used with the TVM_INSERTITEM message. The structure is identical to the TV_INSERTSTRUCT structure, but it has been renamed to follow current naming conventions.
old-location: controls\TVINSERTSTRUCT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\treeview\structures\tvinsertstruct.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*LPTVINSERTSTRUCTW, LPTVINSERTSTRUCT, LPTVINSERTSTRUCT structure pointer [Windows Controls], TVINSERTSTRUCT, TVINSERTSTRUCT structure [Windows Controls], TVINSERTSTRUCTA, TVINSERTSTRUCTW, TVI_FIRST, TVI_LAST, TVI_ROOT, TVI_SORT, _win32_TVINSERTSTRUCT, _win32_TVINSERTSTRUCT_cpp, commctrl/LPTVINSERTSTRUCT, commctrl/TVINSERTSTRUCT, commctrl/TVINSERTSTRUCTA, commctrl/TVINSERTSTRUCTW, controls.TVINSERTSTRUCT, controls._win32_TVINSERTSTRUCT, tagTVINSERTSTRUCTW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TVINSERTSTRUCTW (Unicode) and TVINSERTSTRUCTA (ANSI)
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
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TVINSERTSTRUCT
 - TVINSERTSTRUCTA
 - TVINSERTSTRUCTW
product: Windows
targetos: Windows
req.typenames: TVINSERTSTRUCTW, *LPTVINSERTSTRUCTW
req.redist: 
---

# tagTVINSERTSTRUCTW structure


## -description


Contains information used to add a new item to a tree-view control. This structure is used with the <a href="https://msdn.microsoft.com/c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e">TVM_INSERTITEM</a> message. The structure is identical to the <b>TV_INSERTSTRUCT</b> structure, but it has been renamed to follow current naming conventions. 


## -struct-fields




### -field hParent

Type: <b>HTREEITEM</b>

Handle to the parent item. If this member is the TVI_ROOT value or <b>NULL</b>, the item is inserted at the root of the tree-view control. 


### -field hInsertAfter

Type: <b>HTREEITEM</b>

Handle to the item after which the new item is to be inserted, or one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TVI_FIRST"></a><a id="tvi_first"></a><dl>
<dt><b>TVI_FIRST</b></dt>
</dl>
</td>
<td width="60%">
Inserts the item at the beginning of the list.

</td>
</tr>
<tr>
<td width="40%"><a id="TVI_LAST"></a><a id="tvi_last"></a><dl>
<dt><b>TVI_LAST</b></dt>
</dl>
</td>
<td width="60%">
Inserts the item at the end of the list.

</td>
</tr>
<tr>
<td width="40%"><a id="TVI_ROOT"></a><a id="tvi_root"></a><dl>
<dt><b>TVI_ROOT</b></dt>
</dl>
</td>
<td width="60%">
Add the item as a root item.

</td>
</tr>
<tr>
<td width="40%"><a id="TVI_SORT"></a><a id="tvi_sort"></a><dl>
<dt><b>TVI_SORT</b></dt>
</dl>
</td>
<td width="60%">
Inserts the item into the list in alphabetical order.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.itemex

<b>Type: <b><a href="https://msdn.microsoft.com/a1112639-fe6d-432a-8b0a-b914bcb30e11">TVITEMEX</a></b>
</b>

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.71</a>. <a href="https://msdn.microsoft.com/a1112639-fe6d-432a-8b0a-b914bcb30e11">TVITEMEX</a> structure that contains information about the item to add. 


### -field DUMMYUNIONNAME.item

<b>Type: <b><a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a></b>
</b>

<a href="https://msdn.microsoft.com/8e97f293-3cfb-4320-9781-639dfda1bbfe">TVITEM</a> structure that contains information about the item to add. 


## -remarks



The unions in this structure have been updated to work with compilers that do not support nameless unions. If your compiler does not support nameless unions, define the NONAMELESSUNION token before including the commctrl.h header file.

<div class="alert"><b>Important</b>  Using TVI_LAST to insert an item into a tree-view node that already contains a large number of items can take a long time, causing  the application to stop responding until the insert operation completes.</div>
<div> </div>



---
UID: NS:mmc._RESULTDATAITEM
title: "_RESULTDATAITEM"
author: windows-sdk-content
description: The RESULTDATAITEM structure specifies or receives the attributes of result items in the result pane of the snap-in.
old-location: mmc\resultdataitem.htm
old-project: MMC
ms.assetid: c8f4682e-e1f7-4f7f-9a56-508648ca8c07
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPRESULTDATAITEM, LPRESULTDATAITEM, LPRESULTDATAITEM structure pointer [MMC], LVIS_CUT, LVIS_DROPHILITED, LVIS_FOCUSED, LVIS_SELECTED, RDI_IMAGE, RDI_INDENT, RDI_INDEX, RDI_PARAM, RDI_STATE, RDI_STR, RESULTDATAITEM, RESULTDATAITEM structure [MMC], _RESULTDATAITEM, _slate_resultdataitem, mmc.resultdataitem, mmc/LPRESULTDATAITEM, mmc/RESULTDATAITEM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: RESULTDATAITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - RESULTDATAITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _RESULTDATAITEM structure


## -description


The 
<b>RESULTDATAITEM</b> structure specifies or receives the attributes of result items in the result pane of the snap-in.


## -struct-fields




### -field mask

A set of flags that specifies attributes of this data structure, or  an operation  that uses  this structure.

The following flags specify the members of the 
<b>RESULTDATAITEM</b> structure that  contain valid data, or need to be filled in with data. One or more of the flags can be set.



#### RDI_STR (0x0002)

The <b>str</b> member is valid or must be filled in.



#### RDI_IMAGE (0x0004)

The <b>nImage</b> member is valid or must be filled in.



#### RDI_STATE (0x0008)

The <b>nState</b> member is valid or must be filled in.



#### RDI_PARAM (0x0010)

The <b>lParam</b> member is valid or must be filled in.



#### RDI_INDEX (0x0020)

The <b>nIndex</b> member is valid or must be filled in.



#### RDI_INDENT (0x0040)

The <b>iIndent</b> member is valid or must be filled in.


### -field bScopeItem

<b>TRUE</b> if the <b>lParam</b> member refers to a scope item. <b>FALSE</b> if the <b>lParam</b> member refers to a result item.


### -field itemID

A value that specifies a console-supplied unique item identifier for the result item. This value is used to identify an item in the result pane  of  calls to  some  
<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a> interface methods.

After the snap-in successfully inserts an item in the scope pane (by using <a href="https://msdn.microsoft.com/c354e718-ea9a-4d50-8a77-776500b86d25">IResultData::InsertItem</a>), the <b>itemID</b> member of the 
<b>RESULTDATAITEM</b> structure contains the <b>HRESULTITEM</b> handle of the newly inserted item. This handle is the unique identifier for the result item.

The snap-in should store this value  to  manipulate  (later) the inserted item by calling methods such as <a href="https://msdn.microsoft.com/18c345b0-7d3c-4c80-8d1e-b8d5791bc550">IResultData::GetItem</a>. If this value is not stored, it can be looked up  by using <a href="https://msdn.microsoft.com/f26be5d5-9b7d-4cbd-b70c-431799c68e5e">IResultData::FindItemByLParam</a>.


### -field nIndex

A value that specifies the zero-based index of the item to which this structure refers.


### -field nCol

A value that specifies the column on which an operation is to be performed.  If the operation is to be performed on an item  and not  a  column, the value is zero (0).


### -field str

A pointer to a null-terminated string that contains the item text if the structure specifies the <b>RDI_STR</b> item attribute. If this member is the <b>MMC_CALLBACK</b> value, the item is a callback item.

Be aware that the snap-in can use <b>MMC_TEXTCALLBACK</b> instead of <b>MMC_CALLBACK</b>. The <b>MMC_TEXTCALLBACK</b> value is a type-correct (no casting necessary) version of <b>MMC_CALLBACK</b>.

<b>MMC_TEXTCALLBACK</b> is introduced in MMC version 1.2.


### -field nImage

Virtual image index of the list view item's icon in the large  and small icon image lists. Be aware that the virtual image index is  mapped  internally to the actual index. This member can also be specified as a callback item: <b>MMC_CALLBACK</b> or <b>MMC_IMAGECALLBACK</b>. The <b>MMC_IMAGECALLBACK</b> value is a type-correct (no casting necessary) version of <b>MMC_CALLBACK</b>.

<b>MMC_IMAGECALLBACK</b> is introduced in MMC version 1.2.


### -field nState

A value that specifies the state mask for the item. It can be one of the following values.



#### LVIS_CUT

The item is marked for a cut-and-paste operation.



#### LVIS_DROPHILITED

The item is highlighted as a drag-and-drop target.



#### LVIS_FOCUSED

The item has the focus, so it is surrounded by a standard focus rectangle. More than one item can be selected, but only one item can have the focus.



#### LVIS_SELECTED

The item is selected. The appearance of a selected item depends on whether it has the focus, and on the system colors used for the selection.

<div class="alert"><b>Note</b>  To use the <b>LVIS_*</b> constants, include CommCtrl.h in your source file.</div>
<div> </div>

### -field lParam

A value that specifies a user-supplied 32-bit value to associate with the item. This item, also called a cookie, is the value that is passed as the first parameter to 
<a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">IComponent::QueryDataObject</a>.


### -field iIndent

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>
 

 


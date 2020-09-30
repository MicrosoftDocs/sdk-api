---
UID: NF:winsync.ISyncFilterInfo2.GetFlags
title: ISyncFilterInfo2::GetFlags (winsync.h)
description: Gets the flags that specify additional information about the filter information object.
helpviewer_keywords: ["GetFlags","GetFlags method [Windows Sync]","GetFlags method [Windows Sync]","ISyncFilterInfo2 interface","ISyncFilterInfo2 interface [Windows Sync]","GetFlags method","ISyncFilterInfo2.GetFlags","ISyncFilterInfo2::GetFlags","winsync.isyncfilterinfo2_getflags","winsync/ISyncFilterInfo2::GetFlags"]
old-location: winsync\isyncfilterinfo2_getflags.htm
tech.root: winsync
ms.assetid: cad60957-9d16-4564-b63e-be8e188caecc
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Windows Sync], GetFlags method [Windows Sync],ISyncFilterInfo2 interface, ISyncFilterInfo2 interface [Windows Sync],GetFlags method, ISyncFilterInfo2.GetFlags, ISyncFilterInfo2::GetFlags, winsync.isyncfilterinfo2_getflags, winsync/ISyncFilterInfo2::GetFlags
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncFilterInfo2::GetFlags
 - winsync/ISyncFilterInfo2::GetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncFilterInfo2.GetFlags
---

# ISyncFilterInfo2::GetFlags


## -description

Gets the flags that specify additional information about the filter information object.

## -parameters

### -param pdwFlags [out]

Gets the flags that specify additional information about the filter information object. This will be one of the <b>SYNC_FILTER_INFO_FLAG</b> values (See Remarks).

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -remarks

The following table describes the flags that specify information about an <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo</a> object.

<table>
<tr>
<th>SYNC_FILTER_INFO_FLAG value</th>
<th>Description </th>
</tr>
<tr>
<td><b>SYNC_FILTER_INFO_FLAG_ITEM_LIST</b></td>
<td>This flag indicates that the set of items synchronized is restricted by an item filter.


</td>
</tr>
<tr>
<td><b>SYNC_FILTER_INFO_FLAG_CHANGE_UNIT_LIST</b></td>
<td>An <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitlistfilterinfo">IChangeUnitListFilterInfo</a> object specifies that changes apply only to a subset of the change units that are defined for the scope.
</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitlistfilterinfo">IChangeUnitListFilterInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo2">ISyncFilterInfo2 Interface</a>
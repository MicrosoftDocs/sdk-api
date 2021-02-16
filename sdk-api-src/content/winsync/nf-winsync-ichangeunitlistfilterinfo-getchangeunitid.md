---
UID: NF:winsync.IChangeUnitListFilterInfo.GetChangeUnitId
title: IChangeUnitListFilterInfo::GetChangeUnitId (winsync.h)
description: Gets the change unit ID that is stored at the specified index in the array of change unit IDs that define the filter.
helpviewer_keywords: ["GetChangeUnitId","GetChangeUnitId method [Windows Sync]","GetChangeUnitId method [Windows Sync]","IChangeUnitListFilterInfo interface","IChangeUnitListFilterInfo interface [Windows Sync]","GetChangeUnitId method","IChangeUnitListFilterInfo.GetChangeUnitId","IChangeUnitListFilterInfo::GetChangeUnitId","winsync.ichangeunitlistfilterinfo_getchangeunitid","winsync/IChangeUnitListFilterInfo::GetChangeUnitId"]
old-location: winsync\ichangeunitlistfilterinfo_getchangeunitid.htm
tech.root: winsync
ms.assetid: 67420b58-b3c9-4500-8395-4d176133c142
ms.date: 12/05/2018
ms.keywords: GetChangeUnitId, GetChangeUnitId method [Windows Sync], GetChangeUnitId method [Windows Sync],IChangeUnitListFilterInfo interface, IChangeUnitListFilterInfo interface [Windows Sync],GetChangeUnitId method, IChangeUnitListFilterInfo.GetChangeUnitId, IChangeUnitListFilterInfo::GetChangeUnitId, winsync.ichangeunitlistfilterinfo_getchangeunitid, winsync/IChangeUnitListFilterInfo::GetChangeUnitId
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
 - IChangeUnitListFilterInfo::GetChangeUnitId
 - winsync/IChangeUnitListFilterInfo::GetChangeUnitId
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
 - IChangeUnitListFilterInfo.GetChangeUnitId
---

# IChangeUnitListFilterInfo::GetChangeUnitId


## -description

Gets the change unit ID that is stored at the specified index in the array of change unit IDs that define the filter.

## -parameters

### -param dwChangeUnitIdIndex [in]

The index of the change unit ID to look up.

### -param pbChangeUnitId [in, out]

Returns the change unit ID that is stored at the index that is specified by <i>dwChangeUnitIdIndex</i>.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbChangeUnitId</i>. Returns the number of bytes that are required to retrieve the ID when <i>pbChangeUnitId</i> is too small, or the number of bytes written.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
No filter is defined, or  <i>dwChangeUnitIdIndex</i> is larger than the number of change unit IDs that are stored in this object.


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
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeUnitId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ID_FORMAT_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The change unit ID to be returned is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitlistfilterinfo">IChangeUnitListFilterInfo Interface</a>
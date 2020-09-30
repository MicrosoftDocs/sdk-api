---
UID: NF:winsync.IChangeUnitListFilterInfo.GetChangeUnitIdCount
title: IChangeUnitListFilterInfo::GetChangeUnitIdCount (winsync.h)
description: Gets the number of change unit IDs that define the filter.
helpviewer_keywords: ["GetChangeUnitIdCount","GetChangeUnitIdCount method [Windows Sync]","GetChangeUnitIdCount method [Windows Sync]","IChangeUnitListFilterInfo interface","IChangeUnitListFilterInfo interface [Windows Sync]","GetChangeUnitIdCount method","IChangeUnitListFilterInfo.GetChangeUnitIdCount","IChangeUnitListFilterInfo::GetChangeUnitIdCount","winsync.ichangeunitlistfilterinfo_getchangeunitidcount","winsync/IChangeUnitListFilterInfo::GetChangeUnitIdCount"]
old-location: winsync\ichangeunitlistfilterinfo_getchangeunitidcount.htm
tech.root: winsync
ms.assetid: 23cb5f0f-0b8a-4e98-83b5-9353e7cee5d2
ms.date: 12/05/2018
ms.keywords: GetChangeUnitIdCount, GetChangeUnitIdCount method [Windows Sync], GetChangeUnitIdCount method [Windows Sync],IChangeUnitListFilterInfo interface, IChangeUnitListFilterInfo interface [Windows Sync],GetChangeUnitIdCount method, IChangeUnitListFilterInfo.GetChangeUnitIdCount, IChangeUnitListFilterInfo::GetChangeUnitIdCount, winsync.ichangeunitlistfilterinfo_getchangeunitidcount, winsync/IChangeUnitListFilterInfo::GetChangeUnitIdCount
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
 - IChangeUnitListFilterInfo::GetChangeUnitIdCount
 - winsync/IChangeUnitListFilterInfo::GetChangeUnitIdCount
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
 - IChangeUnitListFilterInfo.GetChangeUnitIdCount
---

# IChangeUnitListFilterInfo::GetChangeUnitIdCount


## -description

Gets the number of change unit IDs that define the filter.

## -parameters

### -param pdwChangeUnitIdCount [out, retval]

Returns the number of change unit IDs that define the filter.

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

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitlistfilterinfo">IChangeUnitListFilterInfo Interface</a>
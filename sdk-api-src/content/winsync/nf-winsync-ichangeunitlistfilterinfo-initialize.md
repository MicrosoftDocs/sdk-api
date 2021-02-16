---
UID: NF:winsync.IChangeUnitListFilterInfo.Initialize
title: IChangeUnitListFilterInfo::Initialize (winsync.h)
description: Initializes a new instance of the IChangeUnitListFilterInfo class that contains the specified array of change unit IDs.
helpviewer_keywords: ["IChangeUnitListFilterInfo interface [Windows Sync]","Initialize method","IChangeUnitListFilterInfo.Initialize","IChangeUnitListFilterInfo::Initialize","Initialize","Initialize method [Windows Sync]","Initialize method [Windows Sync]","IChangeUnitListFilterInfo interface","winsync.ichangeunitlistfilterinfo_initialize","winsync/IChangeUnitListFilterInfo::Initialize"]
old-location: winsync\ichangeunitlistfilterinfo_initialize.htm
tech.root: winsync
ms.assetid: ee3f86dc-8f5a-4b9b-ac06-b836898392ba
ms.date: 12/05/2018
ms.keywords: IChangeUnitListFilterInfo interface [Windows Sync],Initialize method, IChangeUnitListFilterInfo.Initialize, IChangeUnitListFilterInfo::Initialize, Initialize, Initialize method [Windows Sync], Initialize method [Windows Sync],IChangeUnitListFilterInfo interface, winsync.ichangeunitlistfilterinfo_initialize, winsync/IChangeUnitListFilterInfo::Initialize
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
 - IChangeUnitListFilterInfo::Initialize
 - winsync/IChangeUnitListFilterInfo::Initialize
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
 - IChangeUnitListFilterInfo.Initialize
---

# IChangeUnitListFilterInfo::Initialize


## -description

Initializes a new instance of the <b>IChangeUnitListFilterInfo</b> class that contains the specified array of change unit IDs.

## -parameters

### -param ppbChangeUnitIds [in]

The array of change unit IDs that indicate which change units are included by this filter.

### -param dwChangeUnitCount [in]

The number of change unit IDs that are contained in <i>ppbChangeUnitIds</i>.

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
<i>dwChangeUnitCount</i> is 0, or any ID that is contained in <i>ppbChangeUnitIds</i> is not valid.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
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

An <b>IChangeUnitListFilterInfo</b> object can be reused. Calling <b>Initialize</b> more than one time frees any previously contained array of change unit IDs and replaces it with the array that is specified by <i>ppbChangeUnitIds</i>.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitlistfilterinfo">IChangeUnitListFilterInfo Interface</a>
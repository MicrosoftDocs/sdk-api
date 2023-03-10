---
UID: NF:winsync.IFeedClockVectorElement.GetSyncTime
title: IFeedClockVectorElement::GetSyncTime (winsync.h)
description: Gets a SYNC_TIME value that corresponds to the when value for the item.
helpviewer_keywords: ["GetSyncTime","GetSyncTime method [Windows Sync]","GetSyncTime method [Windows Sync]","IFeedClockVectorElement interface","IFeedClockVectorElement interface [Windows Sync]","GetSyncTime method","IFeedClockVectorElement.GetSyncTime","IFeedClockVectorElement::GetSyncTime","winsync.ifeedclockvectorelement_getsynctime","winsync/IFeedClockVectorElement::GetSyncTime"]
old-location: winsync\ifeedclockvectorelement_getsynctime.htm
tech.root: winsync
ms.assetid: f39b3bdf-a37e-4673-a620-5b14109718cb
ms.date: 12/05/2018
ms.keywords: GetSyncTime, GetSyncTime method [Windows Sync], GetSyncTime method [Windows Sync],IFeedClockVectorElement interface, IFeedClockVectorElement interface [Windows Sync],GetSyncTime method, IFeedClockVectorElement.GetSyncTime, IFeedClockVectorElement::GetSyncTime, winsync.ifeedclockvectorelement_getsynctime, winsync/IFeedClockVectorElement::GetSyncTime
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
 - IFeedClockVectorElement::GetSyncTime
 - winsync/IFeedClockVectorElement::GetSyncTime
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
 - IFeedClockVectorElement.GetSyncTime
---

# IFeedClockVectorElement::GetSyncTime


## -description

Gets a <a href="/windows/desktop/api/winsync/ns-winsync-sync_time">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.

## -parameters

### -param pSyncTime [out]

Returns a <a href="/windows/desktop/api/winsync/ns-winsync-sync_time">SYNC_TIME</a> value that corresponds to the <b>when</b> value for the item.

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
<td width="60%"></td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/winsync/ns-winsync-sync_time">SYNC_TIME</a> structure is a packed date-and-time value that can store years between 1601 and 67136 and times that are accurate to the millisecond.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ifeedclockvectorelement">IFeedClockVectorElement Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_time">SYNC_TIME Structure</a>
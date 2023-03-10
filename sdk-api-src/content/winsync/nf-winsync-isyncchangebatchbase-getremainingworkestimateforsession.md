---
UID: NF:winsync.ISyncChangeBatchBase.GetRemainingWorkEstimateForSession
title: ISyncChangeBatchBase::GetRemainingWorkEstimateForSession (winsync.h)
description: Gets the estimate of the remaining work for the session.
helpviewer_keywords: ["GetRemainingWorkEstimateForSession","GetRemainingWorkEstimateForSession method [Windows Sync]","GetRemainingWorkEstimateForSession method [Windows Sync]","ISyncChangeBatchBase interface","ISyncChangeBatchBase interface [Windows Sync]","GetRemainingWorkEstimateForSession method","ISyncChangeBatchBase.GetRemainingWorkEstimateForSession","ISyncChangeBatchBase::GetRemainingWorkEstimateForSession","winsync.isyncchangebatchbase_getremainingworkestimateforsession","winsync/ISyncChangeBatchBase::GetRemainingWorkEstimateForSession"]
old-location: winsync\isyncchangebatchbase_getremainingworkestimateforsession.htm
tech.root: winsync
ms.assetid: 8c1d3cf3-4d84-43c0-91cc-fbc418b8cb20
ms.date: 12/05/2018
ms.keywords: GetRemainingWorkEstimateForSession, GetRemainingWorkEstimateForSession method [Windows Sync], GetRemainingWorkEstimateForSession method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetRemainingWorkEstimateForSession method, ISyncChangeBatchBase.GetRemainingWorkEstimateForSession, ISyncChangeBatchBase::GetRemainingWorkEstimateForSession, winsync.isyncchangebatchbase_getremainingworkestimateforsession, winsync/ISyncChangeBatchBase::GetRemainingWorkEstimateForSession
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
 - ISyncChangeBatchBase::GetRemainingWorkEstimateForSession
 - winsync/ISyncChangeBatchBase::GetRemainingWorkEstimateForSession
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
 - ISyncChangeBatchBase.GetRemainingWorkEstimateForSession
---

# ISyncChangeBatchBase::GetRemainingWorkEstimateForSession


## -description

Gets the estimate of the remaining work for the session.

## -parameters

### -param pdwRemainingWorkForSession [out]

The estimated remaining work for the session. The default value is 0.

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

The work estimate is determined by the provider and is typically understood as the remaining work estimated for a session.

This value is reported in the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onprogress">OnProgress</a> event.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>
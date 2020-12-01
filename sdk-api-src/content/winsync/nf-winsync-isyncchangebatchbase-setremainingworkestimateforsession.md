---
UID: NF:winsync.ISyncChangeBatchBase.SetRemainingWorkEstimateForSession
title: ISyncChangeBatchBase::SetRemainingWorkEstimateForSession (winsync.h)
description: Sets the estimate of the remaining work for the session.
helpviewer_keywords: ["ISyncChangeBatchBase interface [Windows Sync]","SetRemainingWorkEstimateForSession method","ISyncChangeBatchBase.SetRemainingWorkEstimateForSession","ISyncChangeBatchBase::SetRemainingWorkEstimateForSession","SetRemainingWorkEstimateForSession","SetRemainingWorkEstimateForSession method [Windows Sync]","SetRemainingWorkEstimateForSession method [Windows Sync]","ISyncChangeBatchBase interface","winsync.isyncchangebatchbase_setremainingworkestimateforsession","winsync/ISyncChangeBatchBase::SetRemainingWorkEstimateForSession"]
old-location: winsync\isyncchangebatchbase_setremainingworkestimateforsession.htm
tech.root: winsync
ms.assetid: f73d13d9-244e-4ec1-aacd-047331b13a4d
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchBase interface [Windows Sync],SetRemainingWorkEstimateForSession method, ISyncChangeBatchBase.SetRemainingWorkEstimateForSession, ISyncChangeBatchBase::SetRemainingWorkEstimateForSession, SetRemainingWorkEstimateForSession, SetRemainingWorkEstimateForSession method [Windows Sync], SetRemainingWorkEstimateForSession method [Windows Sync],ISyncChangeBatchBase interface, winsync.isyncchangebatchbase_setremainingworkestimateforsession, winsync/ISyncChangeBatchBase::SetRemainingWorkEstimateForSession
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
 - ISyncChangeBatchBase::SetRemainingWorkEstimateForSession
 - winsync/ISyncChangeBatchBase::SetRemainingWorkEstimateForSession
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
 - ISyncChangeBatchBase.SetRemainingWorkEstimateForSession
---

# ISyncChangeBatchBase::SetRemainingWorkEstimateForSession


## -description

Sets the estimate of the remaining work for the session.

## -parameters

### -param dwRemainingWorkForSession [in]

The estimate of the remaining work for the session.

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
</table>

## -remarks

The work estimate is determined by the provider.

This value is reported in the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onprogress">OnProgress</a> event. If this value is set to zero, the <a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onprogress">OnProgress</a> event will fire for each change that is applied during the session. It will pass zero for the completed work and total work.

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>
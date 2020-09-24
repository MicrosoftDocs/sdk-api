---
UID: NF:mfapi.MFEndUnregisterWorkQueueWithMMCSS
title: MFEndUnregisterWorkQueueWithMMCSS function (mfapi.h)
description: Completes an asynchronous request to unregister a work queue from a Multimedia Class Scheduler Service (MMCSS) task.
helpviewer_keywords: ["MFEndUnregisterWorkQueueWithMMCSS","MFEndUnregisterWorkQueueWithMMCSS function [Media Foundation]","eca38d5d-9ca3-442e-80ca-96d8927178a1","mf.mfendunregisterworkqueuewithmmcss","mfapi/MFEndUnregisterWorkQueueWithMMCSS"]
old-location: mf\mfendunregisterworkqueuewithmmcss.htm
tech.root: mf
ms.assetid: eca38d5d-9ca3-442e-80ca-96d8927178a1
ms.date: 12/05/2018
ms.keywords: MFEndUnregisterWorkQueueWithMMCSS, MFEndUnregisterWorkQueueWithMMCSS function [Media Foundation], eca38d5d-9ca3-442e-80ca-96d8927178a1, mf.mfendunregisterworkqueuewithmmcss, mfapi/MFEndUnregisterWorkQueueWithMMCSS
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFEndUnregisterWorkQueueWithMMCSS
 - mfapi/MFEndUnregisterWorkQueueWithMMCSS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFEndUnregisterWorkQueueWithMMCSS
---

# MFEndUnregisterWorkQueueWithMMCSS function


## -description

Completes an asynchronous request to unregister a work queue from a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
</table>

## -remarks

Call this function when the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbeginunregisterworkqueuewithmmcss">MFBeginUnregisterWorkQueueWithMMCSS</a> function completes asynchronously.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
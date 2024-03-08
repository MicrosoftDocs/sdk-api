---
UID: NF:mfapi.MFEndRegisterWorkQueueWithMMCSS
title: MFEndRegisterWorkQueueWithMMCSS function (mfapi.h)
description: Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task. (MFEndRegisterWorkQueueWithMMCSS)
helpviewer_keywords: ["42d71e1a-a538-45d3-bbf4-1835db15bff9","MFEndRegisterWorkQueueWithMMCSS","MFEndRegisterWorkQueueWithMMCSS function [Media Foundation]","mf.mfendregisterworkqueuewithmmcss","mfapi/MFEndRegisterWorkQueueWithMMCSS"]
old-location: mf\mfendregisterworkqueuewithmmcss.htm
tech.root: mf
ms.assetid: 42d71e1a-a538-45d3-bbf4-1835db15bff9
ms.date: 12/05/2018
ms.keywords: 42d71e1a-a538-45d3-bbf4-1835db15bff9, MFEndRegisterWorkQueueWithMMCSS, MFEndRegisterWorkQueueWithMMCSS function [Media Foundation], mf.mfendregisterworkqueuewithmmcss, mfapi/MFEndRegisterWorkQueueWithMMCSS
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
 - MFEndRegisterWorkQueueWithMMCSS
 - mfapi/MFEndRegisterWorkQueueWithMMCSS
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
 - MFEndRegisterWorkQueueWithMMCSS
---

# MFEndRegisterWorkQueueWithMMCSS function


## -description

Completes an asynchronous request to associate a work queue with a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

### -param pdwTaskId [in]

The unique task identifier.

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

Call this function when the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss">MFBeginRegisterWorkQueueWithMMCSS</a> function completes asynchronously.

To unregister the work queue from the MMCSS class, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbeginunregisterworkqueuewithmmcss">MFBeginUnregisterWorkQueueWithMMCSS</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>

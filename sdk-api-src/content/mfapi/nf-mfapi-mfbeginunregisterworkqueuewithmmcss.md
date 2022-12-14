---
UID: NF:mfapi.MFBeginUnregisterWorkQueueWithMMCSS
title: MFBeginUnregisterWorkQueueWithMMCSS function (mfapi.h)
description: Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task. (MFBeginUnregisterWorkQueueWithMMCSS)
helpviewer_keywords: ["MFBeginUnregisterWorkQueueWithMMCSS","MFBeginUnregisterWorkQueueWithMMCSS function [Media Foundation]","e164785f-9899-45f0-805f-b091508e35aa","mf.mfbeginunregisterworkqueuewithmmcss","mfapi/MFBeginUnregisterWorkQueueWithMMCSS"]
old-location: mf\mfbeginunregisterworkqueuewithmmcss.htm
tech.root: mf
ms.assetid: e164785f-9899-45f0-805f-b091508e35aa
ms.date: 12/05/2018
ms.keywords: MFBeginUnregisterWorkQueueWithMMCSS, MFBeginUnregisterWorkQueueWithMMCSS function [Media Foundation], e164785f-9899-45f0-805f-b091508e35aa, mf.mfbeginunregisterworkqueuewithmmcss, mfapi/MFBeginUnregisterWorkQueueWithMMCSS
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
 - MFBeginUnregisterWorkQueueWithMMCSS
 - mfapi/MFBeginUnregisterWorkQueueWithMMCSS
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
 - MFBeginUnregisterWorkQueueWithMMCSS
---

# MFBeginUnregisterWorkQueueWithMMCSS function


## -description

Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param dwWorkQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function. For platform work queues, see <a href="/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>.

### -param pDoneCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param pDoneState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

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

This function unregisters a work queue that was associated with an MMCSS class through the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss">MFBeginRegisterWorkQueueWithMMCSS</a> function.

This function is asynchronous. When the operation completes, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfendunregisterworkqueuewithmmcss">MFEndUnregisterWorkQueueWithMMCSS</a> to complete the asynchronous request.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>

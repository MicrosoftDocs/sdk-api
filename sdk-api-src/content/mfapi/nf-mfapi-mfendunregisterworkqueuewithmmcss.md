---
UID: NF:mfapi.MFEndUnregisterWorkQueueWithMMCSS
title: MFEndUnregisterWorkQueueWithMMCSS function (mfapi.h)
author: windows-sdk-content
description: Completes an asynchronous request to unregister a work queue from a Multimedia Class Scheduler Service (MMCSS) task.
old-location: mf\mfendunregisterworkqueuewithmmcss.htm
tech.root: medfound
ms.assetid: eca38d5d-9ca3-442e-80ca-96d8927178a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFEndUnregisterWorkQueueWithMMCSS, MFEndUnregisterWorkQueueWithMMCSS function [Media Foundation], eca38d5d-9ca3-442e-80ca-96d8927178a1, mf.mfendunregisterworkqueuewithmmcss, mfapi/MFEndUnregisterWorkQueueWithMMCSS
ms.topic: function
f1_keywords: 
 - "mfapi/MFEndUnregisterWorkQueueWithMMCSS"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFEndUnregisterWorkQueueWithMMCSS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFEndUnregisterWorkQueueWithMMCSS function


## -description



Completes an asynchronous request to unregister a work queue from a Multimedia Class Scheduler Service (MMCSS) task.




## -parameters




### -param pResult [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.


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



Call this function when the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfbeginunregisterworkqueuewithmmcss">MFBeginUnregisterWorkQueueWithMMCSS</a> function completes asynchronously.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 


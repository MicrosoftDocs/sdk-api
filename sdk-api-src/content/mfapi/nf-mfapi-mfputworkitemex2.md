---
UID: NF:mfapi.MFPutWorkItemEx2
title: MFPutWorkItemEx2 function (mfapi.h)
description: Puts an asynchronous operation on a work queue, with a specified priority. (MFPutWorkItemEx2)
helpviewer_keywords: ["MFPutWorkItemEx2","MFPutWorkItemEx2 function [Media Foundation]","mf.mfputworkitemex2","mfapi/MFPutWorkItemEx2"]
old-location: mf\mfputworkitemex2.htm
tech.root: mf
ms.assetid: A29DC852-AF0F-4269-97FB-DA1F725E7C09
ms.date: 12/05/2018
ms.keywords: MFPutWorkItemEx2, MFPutWorkItemEx2 function [Media Foundation], mf.mfputworkitemex2, mfapi/MFPutWorkItemEx2
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - MFPutWorkItemEx2
 - mfapi/MFPutWorkItemEx2
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
 - MFPutWorkItemEx2
---

# MFPutWorkItemEx2 function


## -description

Puts an asynchronous operation on a work queue, with a specified priority.

## -parameters

### -param dwQueue [in]

The identifier for the work queue. This value can specify one of the standard Media Foundation work queues, or a work queue created by the application. For list of standard Media Foundation work queues, see <a href="/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>. To create a new work queue, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> or  <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex">MFAllocateWorkQueueEx</a>.

### -param Priority [in]

The priority of the work item. This value should be 1, 0, or -1. Items with a value of 1 are executed before items with a value of 0. Items with a value of  -1 are executed after items with a value of 0.

### -param pResult [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult">MFCreateAsyncResult</a>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALID_WORKQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Invalid work queue identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> function was not called, or <a href="/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> was called.

</td>
</tr>
</table>

## -remarks

To invoke the work item, this function passes <i>pResult</i> to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback">MFInvokeCallback</a> function. The callback is specified when you create the result object specified by <i>pResult</i>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>

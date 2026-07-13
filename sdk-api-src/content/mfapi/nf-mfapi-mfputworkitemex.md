---
UID: NF:mfapi.MFPutWorkItemEx
title: MFPutWorkItemEx function (mfapi.h)
description: Puts an asynchronous operation on a work queue. (MFPutWorkItemEx)
helpviewer_keywords: ["67b4f7c6-0d49-4ed0-9bc3-e583451884af","MFPutWorkItemEx","MFPutWorkItemEx function [Media Foundation]","mf.mfputworkitemex","mfapi/MFPutWorkItemEx"]
old-location: mf\mfputworkitemex.htm
tech.root: mf
ms.assetid: 67b4f7c6-0d49-4ed0-9bc3-e583451884af
ms.date: 12/05/2018
ms.keywords: 67b4f7c6-0d49-4ed0-9bc3-e583451884af, MFPutWorkItemEx, MFPutWorkItemEx function [Media Foundation], mf.mfputworkitemex, mfapi/MFPutWorkItemEx
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
 - MFPutWorkItemEx
 - mfapi/MFPutWorkItemEx
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
 - MFPutWorkItemEx
---

# MFPutWorkItemEx function


## -description

Puts an asynchronous operation on a work queue.

## -parameters

### -param dwQueue [in]

The identifier for the work queue. This value can specify one of the standard Media Foundation work queues, or a work queue created by the application. For list of standard Media Foundation work queues, see <a href="/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>. To create a new work queue, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex">MFAllocateWorkQueueEx</a>.

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
Invalid work queue identifier. For more information, see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters">IMFAsyncCallback::GetParameters</a>.

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

To invoke the work-item, this function passes <i>pResult</i> to the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback">MFInvokeCallback</a> function. The callback is specified when you create the result object specified by <i>pResult</i>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem">MFPutWorkItem</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>

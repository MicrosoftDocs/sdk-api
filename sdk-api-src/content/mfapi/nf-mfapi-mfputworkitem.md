---
UID: NF:mfapi.MFPutWorkItem
title: MFPutWorkItem function (mfapi.h)
description: Puts an asynchronous operation on a work queue. (MFPutWorkItem)
helpviewer_keywords: ["MFPutWorkItem","MFPutWorkItem function [Media Foundation]","b0233589-2a55-4803-9dcb-85d757734dee","mf.mfputworkitem","mfapi/MFPutWorkItem"]
old-location: mf\mfputworkitem.htm
tech.root: mf
ms.assetid: b0233589-2a55-4803-9dcb-85d757734dee
ms.date: 12/05/2018
ms.keywords: MFPutWorkItem, MFPutWorkItem function [Media Foundation], b0233589-2a55-4803-9dcb-85d757734dee, mf.mfputworkitem, mfapi/MFPutWorkItem
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
 - MFPutWorkItem
 - mfapi/MFPutWorkItem
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
 - MFPutWorkItem
---

# MFPutWorkItem function


## -description

Puts an asynchronous operation on a work queue.

## -parameters

### -param dwQueue [in]

The identifier for the work queue. This value can specify one of the standard Media Foundation work queues, or a work queue created by the application. For list of standard Media Foundation work queues, see <a href="/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>. To create a new work queue, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex">MFAllocateWorkQueueEx</a>.

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface. The caller must implement this interface.

### -param pState [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

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
Invalid work queue. For more information, see <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters">IMFAsyncCallback::GetParameters</a>.

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

This function creates an asynchronous result object and puts the result object on the work queue. The work queue calls the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method specified by <i>pCallback</i>.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex">MFPutWorkItemEx</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>

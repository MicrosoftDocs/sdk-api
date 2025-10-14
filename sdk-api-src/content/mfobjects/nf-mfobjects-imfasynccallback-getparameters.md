---
UID: NF:mfobjects.IMFAsyncCallback.GetParameters
title: IMFAsyncCallback::GetParameters (mfobjects.h)
description: Provides configuration information to the dispatching thread for a callback. (IMFAsyncCallback.GetParameters)
helpviewer_keywords: ["374dd139-d3e7-45d0-a7d3-1187b928ef57","GetParameters","GetParameters method [Media Foundation]","GetParameters method [Media Foundation]","IMFAsyncCallback interface","IMFAsyncCallback interface [Media Foundation]","GetParameters method","IMFAsyncCallback.GetParameters","IMFAsyncCallback::GetParameters","MFASYNC_BLOCKING_CALLBACK","MFASYNC_FAST_IO_PROCESSING_CALLBACK","MFASYNC_REPLY_CALLBACK","MFASYNC_SIGNAL_CALLBACK","Zero","mf.imfasynccallback_getparameters","mfobjects/IMFAsyncCallback::GetParameters"]
old-location: mf\imfasynccallback_getparameters.htm
tech.root: mf
ms.assetid: 374dd139-d3e7-45d0-a7d3-1187b928ef57
ms.date: 12/05/2018
ms.keywords: 374dd139-d3e7-45d0-a7d3-1187b928ef57, GetParameters, GetParameters method [Media Foundation], GetParameters method [Media Foundation],IMFAsyncCallback interface, IMFAsyncCallback interface [Media Foundation],GetParameters method, IMFAsyncCallback.GetParameters, IMFAsyncCallback::GetParameters, MFASYNC_BLOCKING_CALLBACK, MFASYNC_FAST_IO_PROCESSING_CALLBACK, MFASYNC_REPLY_CALLBACK, MFASYNC_SIGNAL_CALLBACK, Zero, mf.imfasynccallback_getparameters, mfobjects/IMFAsyncCallback::GetParameters
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAsyncCallback::GetParameters
 - mfobjects/IMFAsyncCallback::GetParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAsyncCallback.GetParameters
---

# IMFAsyncCallback::GetParameters


## -description

Provides configuration information to the dispatching thread for a callback.

## -parameters

### -param pdwFlags [out]

Receives a flag indicating the behavior of the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method. The following values are defined. The default value is zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Zero"></a><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>Zero</b></dt>
</dl>
</td>
<td width="60%">
The callback does not take a long time to complete, but has no specific restrictions on what system calls it makes. The callback generally takes less than 30 milliseconds to complete.

</td>
</tr>
<tr>
<td width="40%"><a id="MFASYNC_FAST_IO_PROCESSING_CALLBACK"></a><a id="mfasync_fast_io_processing_callback"></a><dl>
<dt><b>MFASYNC_FAST_IO_PROCESSING_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The callback does very minimal processing. It takes less than 1 millisecond to complete.

The callback must be invoked from one of the following work queues:

<ul>
<li><b>MFASYNC_CALLBACK_QUEUE_IO</b></li>
<li><b>MFASYNC_CALLBACK_QUEUE_TIMER</b></li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="MFASYNC_SIGNAL_CALLBACK"></a><a id="mfasync_signal_callback"></a><dl>
<dt><b>MFASYNC_SIGNAL_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Implies <b>MFASYNC_FAST_IO_PROCESSING_CALLBACK</b>, with the additional restriction that the callback does no processing (less than 50 microseconds), and the only system call it makes is <b>SetEvent</b>.

The callback must be invoked from one of the following work queues:

<ul>
<li><b>MFASYNC_CALLBACK_QUEUE_IO</b></li>
<li><b>MFASYNC_CALLBACK_QUEUE_TIMER</b></li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="MFASYNC_BLOCKING_CALLBACK"></a><a id="mfasync_blocking_callback"></a><dl>
<dt><b>MFASYNC_BLOCKING_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Blocking callback.

</td>
</tr>
<tr>
<td width="40%"><a id="MFASYNC_REPLY_CALLBACK"></a><a id="mfasync_reply_callback"></a><dl>
<dt><b>MFASYNC_REPLY_CALLBACK</b></dt>
</dl>
</td>
<td width="60%">
Reply callback.

</td>
</tr>
</table>

### -param pdwQueue [out]

Receives the identifier of the work queue on which the callback is dispatched. 
          

This value can specify one of the standard Media Foundation work queues, or a work queue created by the application. For list of standard Media Foundation work queues, see <a href="/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>. To create a new work queue, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a>. The default value is <b>MFASYNC_CALLBACK_QUEUE_STANDARD</b>.

If the work queue is not compatible with the value returned in <i>pdwFlags</i>, the Media Foundation platform returns <b>MF_E_INVALID_WORKQUEUE</b> when it tries to dispatch the callback. (See <a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem">MFPutWorkItem</a>.)

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Assume the default behavior.
              

</td>
</tr>
</table>

## -remarks

The <b>GetParameters</b> method returns information about the callback so that the dispatching thread can optimize the process that it uses to invoke the callback.
      

If the method returns a value other than zero in the <i>pdwFlags</i> parameter, your <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a> method must meet the requirements described here. Otherwise, the callback might delay the pipeline.

If you want default values for both parameters, return <b>E_NOTIMPL</b>. The default values are given in the parameter descriptions on this page.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>

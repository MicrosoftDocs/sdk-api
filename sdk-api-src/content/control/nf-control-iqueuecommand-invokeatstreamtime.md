---
UID: NF:control.IQueueCommand.InvokeAtStreamTime
title: IQueueCommand::InvokeAtStreamTime (control.h)
description: The InvokeAtStreamTime method queues a method or property change for execution at a specified stream time (that is, presentation time relative to the current stream time offset).
helpviewer_keywords: ["IQueueCommand interface [DirectShow]","InvokeAtStreamTime method","IQueueCommand.InvokeAtStreamTime","IQueueCommand::InvokeAtStreamTime","IQueueCommandInvokeAtStreamTime","InvokeAtStreamTime","InvokeAtStreamTime method [DirectShow]","InvokeAtStreamTime method [DirectShow]","IQueueCommand interface","control/IQueueCommand::InvokeAtStreamTime","dshow.iqueuecommand_invokeatstreamtime"]
old-location: dshow\iqueuecommand_invokeatstreamtime.htm
tech.root: dshow
ms.assetid: 350b6842-207c-47db-a3f8-9e2784d9da67
ms.date: 4/26/2023
ms.keywords: IQueueCommand interface [DirectShow],InvokeAtStreamTime method, IQueueCommand.InvokeAtStreamTime, IQueueCommand::InvokeAtStreamTime, IQueueCommandInvokeAtStreamTime, InvokeAtStreamTime, InvokeAtStreamTime method [DirectShow], InvokeAtStreamTime method [DirectShow],IQueueCommand interface, control/IQueueCommand::InvokeAtStreamTime, dshow.iqueuecommand_invokeatstreamtime
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueueCommand::InvokeAtStreamTime
 - control/IQueueCommand::InvokeAtStreamTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IQueueCommand.InvokeAtStreamTime
---

# IQueueCommand::InvokeAtStreamTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>InvokeAtStreamTime</code> method queues a method or property change for execution at a specified stream time (that is, presentation time relative to the current stream time offset).

## -parameters

### -param pCmd [out]

Address of a variable that receives an <a href="/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand</a> interface pointer.

### -param time [in]

Time at which to invoke the command.

### -param iid [in]

Pointer to the interface identifier (IID) of interface.

### -param dispidMethod [in]

Dispatch identifier (DISPID) of a method or property on the interface. Equivalent to the <i>dispIdMember</i> parameter of the <b>IDispatch::Invoke</b> method.

### -param wFlags [in]

Flags describing the context of the call. Equivalent to the <i>wFlags</i> parameter of the <b>IDispatch::Invoke</b> method.

### -param cArgs [in]

Number of arguments in <i>pDispParams</i>. Equivalent to the <b>cArgs</b> member of the <b>DISPPARAMS</b> structure.

### -param pDispParams [in]

Pointer to an array that contains the arguments. Equivalent to the <b>rgvarg</b> member of the <b>DISPPARAMS</b> structure.

### -param pvarResult [in, out]

Pointer to a VARIANT that receives the result. Equivalent to the <i>pVarResult</i> parameter of the <b>IDispatch::Invoke</b> method.

### -param puArgErr [out]

Pointer to a variable that receives the index of the first argument that has an error. Equivalent to the <i>puArgErr</i> parameter of the <b>IDispatch::Invoke</b> method.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Use the <b>IDispatch::GetIDsOfNames</b> method to retrieve the DISPID for the <i>dispidMember</i> parameter.


#### Examples

The following example queues an <a href="/windows/desktop/api/control/nf-control-imediacontrol-stop">IMediaControl::Stop</a> command for 3.0 seconds.


```cpp

IQueueCommand *pQ = 0;
IMediaControl *pControl = 0;

// Query for IQueueCommand.
pGraph->QueryInterface(IID_IQueueCommand, reinterpret_cast<void**>(&pQ));

// Query for IMediaControl.
pGraph->QueryInterface(IID_IMediaControl, reinterpret_cast<void**>(&pControl));

// Find the DISPID of the IMediaControl::Stop method.
OLECHAR *szMethod = OLESTR("Stop");

long dispid;
hr = pControl->GetIDsOfNames(IID_NULL, &szMethod, 1, 0, &dispid);

// Invoke the command.
IDeferredCommand *pCmd = 0;
hr = pQ->InvokeAtPresentationTime(&pCmd, 3.0,
    const_cast<GUID*>(&IID_IMediaControl), dispid, DISPATCH_METHOD, 
    0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    pControl->Run();
    pCmd->Release();
}

```

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-iqueuecommand">IQueueCommand Interface</a>
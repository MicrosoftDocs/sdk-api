---
UID: NF:control.IMediaEvent.WaitForCompletion
title: IMediaEvent::WaitForCompletion (control.h)
description: The WaitForCompletion method waits for the filter graph to render all available data. The filter graph must be running or the method fails.
helpviewer_keywords: ["IMediaEvent interface [DirectShow]","WaitForCompletion method","IMediaEvent.WaitForCompletion","IMediaEvent::WaitForCompletion","IMediaEventWaitForCompletion","WaitForCompletion","WaitForCompletion method [DirectShow]","WaitForCompletion method [DirectShow]","IMediaEvent interface","control/IMediaEvent::WaitForCompletion","dshow.imediaevent_waitforcompletion"]
old-location: dshow\imediaevent_waitforcompletion.htm
tech.root: dshow
ms.assetid: 760a90fe-7cbc-4f09-ba64-afe0ab0b4c74
ms.date: 12/05/2018
ms.keywords: IMediaEvent interface [DirectShow],WaitForCompletion method, IMediaEvent.WaitForCompletion, IMediaEvent::WaitForCompletion, IMediaEventWaitForCompletion, WaitForCompletion, WaitForCompletion method [DirectShow], WaitForCompletion method [DirectShow],IMediaEvent interface, control/IMediaEvent::WaitForCompletion, dshow.imediaevent_waitforcompletion
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
 - IMediaEvent::WaitForCompletion
 - control/IMediaEvent::WaitForCompletion
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
 - IMediaEvent.WaitForCompletion
---

# IMediaEvent::WaitForCompletion


## -description

The <code>WaitForCompletion</code> method waits for the filter graph to render all available data. The filter graph must be running or the method fails.

## -parameters

### -param msTimeout [in]

Time-out interval, in milliseconds. Pass zero to return immediately. Pass the value INFINITE to block indefinitely.

### -param pEvCode [out]

Pointer to a variable that receives an event code. See Remarks for more information.

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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
Time-out expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The filter graph is not running.

</td>
</tr>
</table>

## -remarks

This method blocks until the time-out expires, or one of the following events occurs:

<ul>
<li>
<a href="/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-errorabort">EC_ERRORABORT</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/ec-userabort">EC_USERABORT</a>
</li>
</ul>
During the wait, the method discards all other event notifications.

If the return value is S_OK, the <i>pEvCode</i> parameter receives the event code that ended the wait. When the method returns, the filter graph is still running. The application can pause or stop the graph, as appropriate.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-imediaevent">IMediaEvent Interface</a>
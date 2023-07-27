---
UID: NF:strmif.IPinFlowControl.Block
title: IPinFlowControl::Block (strmif.h)
description: The Block method blocks or unblocks the flow of data from the pin.
helpviewer_keywords: ["Block","Block method [DirectShow]","Block method [DirectShow]","IPinFlowControl interface","IPinFlowControl interface [DirectShow]","Block method","IPinFlowControl.Block","IPinFlowControl::Block","IPinFlowControlBlock","dshow.ipinflowcontrol_block","strmif/IPinFlowControl::Block"]
old-location: dshow\ipinflowcontrol_block.htm
tech.root: dshow
ms.assetid: 9bcd325d-41fc-4166-8fce-50fc921efdba
ms.date: 4/26/2023
ms.keywords: Block, Block method [DirectShow], Block method [DirectShow],IPinFlowControl interface, IPinFlowControl interface [DirectShow],Block method, IPinFlowControl.Block, IPinFlowControl::Block, IPinFlowControlBlock, dshow.ipinflowcontrol_block, strmif/IPinFlowControl::Block
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IPinFlowControl::Block
 - strmif/IPinFlowControl::Block
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
 - IPinFlowControl.Block
---

# IPinFlowControl::Block


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Block</code> method blocks or unblocks the flow of data from the pin.

## -parameters

### -param dwBlockFlags [in]

Flag that indicates whether to block or unblock the pin. Must be one of the following values:

<ul>
<li>Zero: Unblock data flow from the pin.</li>
<li>AM_PIN_FLOW_CONTROL_BLOCK: Block data flow from the pin.</li>
</ul>

### -param hEvent [in]

Handle to an event object, or <b>NULL</b>. If this parameter is non-<b>NULL</b>, the method is asynchronous and returns immediately. The event is signaled when the operation completes. If this parameter is <b>NULL</b>, the method is synchronous and does not complete until the pin is blocked. If <i>dwBlockFlags</i> is zero, this parameter must be <b>NULL</b>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Pin is already unblocked.

</td>
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
<dt><b>VFW_E_PIN_ALREADY_BLOCKED</b></dt>
</dl>
</td>
<td width="60%">
Pin is already blocked on another thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_PIN_ALREADY_BLOCKED_ON_THIS_THREAD</b></dt>
</dl>
</td>
<td width="60%">
Pin is already blocked on the calling thread.

</td>
</tr>
</table>

## -remarks

This method can be synchronous or asynchronous:

<ul>
<li>To call it asynchronously, use the <b>CreateEvent</b> function to create an event object. Pass the event handle in the <i>hEvent</i> parameter. The method returns immediately and signals the event when the operation has completed. Call a wait function such as <b>WaitForSingleObject</b> to wait for the event.</li>
<li>To call this method synchronously, set the <i>hEvent</i> parameter to <b>NULL</b>. The method blocks until it completes. The method might not complete until the pin is ready to deliver a sample. If the filter is paused, the method might block indefinitely. Therefore, you should not call this method synchronously from your main application thread.</li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipinflowcontrol">IPinFlowControl Interface</a>
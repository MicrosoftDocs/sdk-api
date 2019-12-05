---
UID: NN:ctffunc.IUIManagerEventSink
title: IUIManagerEventSink (ctffunc.h)
description: The IUIManagerEventSink interface is implemented by an app supporting IME UI integration to receive notifications of IME UI appearance.
old-location: tsf\iuimanagereventsink.htm
tech.root: TSF
ms.assetid: A514833B-BC60-4D87-B2C6-849003E4EA63
ms.date: 12/05/2018
ms.keywords: IUIManagerEventSink, IUIManagerEventSink interface [Text Services Framework], IUIManagerEventSink interface [Text Services Framework],described, ctffunc/IUIManagerEventSink, tsf.iuimanagereventsink
ms.topic: interface
f1_keywords:
- ctffunc/IUIManagerEventSink
dev_langs:
- c++
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ctffunc.h
api_name:
- IUIManagerEventSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIManagerEventSink interface


## -description


The <b>IUIManagerEventSink</b> interface is implemented by an app supporting IME UI integration to receive notifications of IME UI appearance. This enables the app to rearrange its UI layout to avoid having the app's UI elements overlapped by the IME UI.

Call the TSF manager <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with <b>IID_IUIManagerEventSink</b> to install this sink.
<div class="alert"><b>Note</b>  This interface may not be supported for all IMEs. There may be differences in support between IME on the Desktop and IME in the new Windows UI on Windows 8.1.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIManagerEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIManagerEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIManagerEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-iuimanagereventsink-onwindowclosed">OnWindowClosed</a>
</td>
<td align="left" width="63%">
Called by the TSF after closing the IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-iuimanagereventsink-onwindowclosing">OnWindowClosing</a>
</td>
<td align="left" width="63%">
Called by the TSF before closing the IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-iuimanagereventsink-onwindowopened">OnWindowOpened</a>
</td>
<td align="left" width="63%">
Called by the TSF after opening an IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-iuimanagereventsink-onwindowopening">OnWindowOpening</a>
</td>
<td align="left" width="63%">
Called by the TSF before opening an IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-iuimanagereventsink-onwindowupdated">OnWindowUpdated</a>
</td>
<td align="left" width="63%">
Called by the TSF after resizing and/or relocating the opened IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nf-ctffunc-iuimanagereventsink-onwindowupdating">OnWindowUpdating</a>
</td>
<td align="left" width="63%">
Called by the TSF before resizing and/or relocating the opened IME
UI.

</td>
</tr>
</table> 


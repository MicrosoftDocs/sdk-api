---
UID: NN:ctffunc.IUIManagerEventSink
title: IUIManagerEventSink
author: windows-sdk-content
description: The IUIManagerEventSink interface is implemented by an app supporting IME UI integration to receive notifications of IME UI appearance.
old-location: tsf\iuimanagereventsink.htm
tech.root: TSF
ms.assetid: A514833B-BC60-4D87-B2C6-849003E4EA63
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIManagerEventSink, IUIManagerEventSink interface [Text Services Framework], IUIManagerEventSink interface [Text Services Framework],described, ctffunc/IUIManagerEventSink, tsf.iuimanagereventsink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIManagerEventSink interface


## -description


The <b>IUIManagerEventSink</b> interface is implemented by an app supporting IME UI integration to receive notifications of IME UI appearance. This enables the app to rearrange its UI layout to avoid having the app's UI elements overlapped by the IME UI.

Call the TSF manager <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with <b>IID_IUIManagerEventSink</b> to install this sink.
<div class="alert"><b>Note</b>  This interface may not be supported for all IMEs. There may be differences in support between IME on the Desktop and IME in the new Windows UI on Windows 8.1.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIManagerEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIManagerEventSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/F63D022D-30EC-430C-8ACE-8EBD97AB8B6A">OnWindowClosed</a>
</td>
<td align="left" width="63%">
Called by the TSF after closing the IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1350286D-522D-4549-B69C-31874352AEAD">OnWindowClosing</a>
</td>
<td align="left" width="63%">
Called by the TSF before closing the IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/525500C2-313E-4430-88B1-AA1F54A420AF">OnWindowOpened</a>
</td>
<td align="left" width="63%">
Called by the TSF after opening an IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B384AC51-2544-429B-ADEC-1D45CCB178FB">OnWindowOpening</a>
</td>
<td align="left" width="63%">
Called by the TSF before opening an IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A50F3F1B-B00A-4ABD-B94A-F1D3904C6938">OnWindowUpdated</a>
</td>
<td align="left" width="63%">
Called by the TSF after resizing and/or relocating the opened IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BCCE292C-8A74-4DBA-965D-15249E2EA547">OnWindowUpdating</a>
</td>
<td align="left" width="63%">
Called by the TSF before resizing and/or relocating the opened IME
UI.

</td>
</tr>
</table> 


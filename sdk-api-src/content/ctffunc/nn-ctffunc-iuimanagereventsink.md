---
UID: NN:ctffunc.IUIManagerEventSink
title: IUIManagerEventSink
author: windows-sdk-content
description: The IUIManagerEventSink interface is implemented by an app supporting IME UI integration to receive notifications of IME UI appearance.
old-location: tsf\iuimanagereventsink.htm
tech.root: TSF
ms.assetid: A514833B-BC60-4D87-B2C6-849003E4EA63
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IUIManagerEventSink, IUIManagerEventSink interface [Text Services Framework], IUIManagerEventSink interface [Text Services Framework],described, ctffunc/IUIManagerEventSink, tsf.iuimanagereventsink
ms.prod: windows
ms.technology: windows-sdk
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

Call the TSF manager <a href="https://msdn.microsoft.com/en-us/library/ms628945(v=VS.85).aspx">ITfSource::AdviseSink</a> with <b>IID_IUIManagerEventSink</b> to install this sink.
<div class="alert"><b>Note</b>  This interface may not be supported for all IMEs. There may be differences in support between IME on the Desktop and IME in the new Windows UI on Windows 8.1.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIManagerEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IUIManagerEventSink</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn495082(v=VS.85).aspx">OnWindowClosed</a>
</td>
<td align="left" width="63%">
Called by the TSF after closing the IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn495083(v=VS.85).aspx">OnWindowClosing</a>
</td>
<td align="left" width="63%">
Called by the TSF before closing the IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn495084(v=VS.85).aspx">OnWindowOpened</a>
</td>
<td align="left" width="63%">
Called by the TSF after opening an IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn495085(v=VS.85).aspx">OnWindowOpening</a>
</td>
<td align="left" width="63%">
Called by the TSF before opening an IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn495086(v=VS.85).aspx">OnWindowUpdated</a>
</td>
<td align="left" width="63%">
Called by the TSF after resizing and/or relocating the opened IME
UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn495087(v=VS.85).aspx">OnWindowUpdating</a>
</td>
<td align="left" width="63%">
Called by the TSF before resizing and/or relocating the opened IME
UI.

</td>
</tr>
</table> 


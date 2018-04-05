---
UID: NN:msctf.ITfUIElementSink
title: ITfUIElementSink
author: windows-driver-content
description: The ITfUIElementSink interface is implemented by an application to receive notifications when the UI element is changed.
old-location: tsf\itfuielementsink.htm
old-project: TSF
ms.assetid: 8f77b3bc-2e47-4966-8030-d05a626ee00a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfUIElementSink, ITfUIElementSink interface [Text Services Framework], ITfUIElementSink interface [Text Services Framework], described, _tsf_itfuielementsink_ref, msctf/ITfUIElementSink, tsf.itfuielementsink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.h
api_name:
-	ITfUIElementSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfUIElementSink interface


## -description


The <b>ITfUIElementSink</b> interface is implemented by an application to receive notifications when the UI element is changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfUIElementSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfUIElementSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfUIElementSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/068c6963-7d69-45b9-8f8b-7af358548a56">BeginUIElement</a>
</td>
<td align="left" width="63%">
This is called when the UIElement started. This sink can let the textservice to draw or not to draw the UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b29539fe-a240-498b-8267-be243d437005">EndUIElement</a>
</td>
<td align="left" width="63%">
This is called when the UIElement is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/573742f6-df34-4336-a090-3d03a90946ec">UpdateUIElement</a>
</td>
<td align="left" width="63%">
This is called when the contents of the UIElement is updated.

</td>
</tr>
</table> 


## -remarks



To install this advise sink, obtain an <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> object from an <a href="https://msdn.microsoft.com/7b4d3f4e-bf30-45c6-8709-88b71b25d333">ITfUIElementMgr</a> object by calling <b>ITfUIElementMgr::QueryInterface</b> with IID_ ITfSource. Then call <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ ITfUIElementSink.




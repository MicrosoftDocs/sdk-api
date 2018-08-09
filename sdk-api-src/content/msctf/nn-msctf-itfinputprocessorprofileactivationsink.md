---
UID: NN:msctf.ITfInputProcessorProfileActivationSink
title: ITfInputProcessorProfileActivationSink
author: windows-sdk-content
description: The ITfInputProcessorProfileActivationSink interface is implemented by an application to receive notifications when the profile changes.
old-location: tsf\itfinputprocessorprofileactivationsink.htm
old-project: TSF
ms.assetid: 97a6a820-8e0e-46b0-a359-da0a17fb4cae
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfInputProcessorProfileActivationSink, ITfInputProcessorProfileActivationSink interface [Text Services Framework], ITfInputProcessorProfileActivationSink interface [Text Services Framework],described, _tsf_itfinputprocessorprofileactivationsink_ref, msctf/ITfInputProcessorProfileActivationSink, tsf.itfinputprocessorprofileactivationsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfInputProcessorProfileActivationSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfileActivationSink interface


## -description


The <b>ITfInputProcessorProfileActivationSink</b> interface is implemented by an application to receive notifications when the profile changes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfInputProcessorProfileActivationSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfInputProcessorProfileActivationSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfInputProcessorProfileActivationSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d171cf73-b409-4501-a956-06867c20f214">OnActivated</a>
</td>
<td align="left" width="63%">
Callback method that is called when an input processor profile is activated or deactivated.

</td>
</tr>
</table> 


## -remarks



To install this advise sink, obtain an <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> object from an <a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a> object by calling <b>ITfThreadMgr::QueryInterface</b> with <b>IID_ ITfSource</b>. Then call <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with <b>IID_ITfInputProcessorProfileActivationSink</b>.




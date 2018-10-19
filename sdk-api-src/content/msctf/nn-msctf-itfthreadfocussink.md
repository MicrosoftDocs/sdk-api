---
UID: NN:msctf.ITfThreadFocusSink
title: ITfThreadFocusSink
author: windows-sdk-content
description: The ITfThreadFocusSink interface is implemented by an application or TSF text service to receive notifications when the thread receives or loses the UI focus.
old-location: tsf\itfthreadfocussink.htm
tech.root: TSF
ms.assetid: 17335fa9-01ee-4585-9454-f326b6281ab1
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfThreadFocusSink, ITfThreadFocusSink interface [Text Services Framework], ITfThreadFocusSink interface [Text Services Framework],described, _tsf_itfthreadfocussink_ref, msctf/ITfThreadFocusSink, tsf.itfthreadfocussink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfThreadFocusSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfThreadFocusSink interface


## -description


The <b>ITfThreadFocusSink</b> interface is implemented by an application or TSF text service to receive notifications when the thread receives or loses the UI focus. This advise sink is installed by calling the TSF Manager's <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfThreadFocusSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadFocusSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfThreadFocusSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfThreadFocusSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea4034e3-e5c1-471e-ae9c-398ab7dbfe67">OnKillThreadFocus</a>
</td>
<td align="left" width="63%">
Called when the thread loses the UI focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b126f83-74ee-4430-bb07-d4069f899c25">OnSetThreadFocus</a>
</td>
<td align="left" width="63%">
Called when the thread receives the UI focus.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 


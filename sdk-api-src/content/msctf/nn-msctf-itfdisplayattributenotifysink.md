---
UID: NN:msctf.ITfDisplayAttributeNotifySink
title: ITfDisplayAttributeNotifySink
author: windows-sdk-content
description: The ITfDisplayAttributeNotifySink interface is implemented by an application to receive a notification when display attribute information is updated.
old-location: tsf\itfdisplayattributenotifysink.htm
tech.root: TSF
ms.assetid: c21ff404-af42-488a-90f0-d3f02277c557
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfDisplayAttributeNotifySink, ITfDisplayAttributeNotifySink interface [Text Services Framework], ITfDisplayAttributeNotifySink interface [Text Services Framework],described, _tsf_itfdisplayattributenotifysink_ref, msctf/ITfDisplayAttributeNotifySink, tsf.itfdisplayattributenotifysink
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfDisplayAttributeNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfDisplayAttributeNotifySink interface


## -description


The <b>ITfDisplayAttributeNotifySink</b> interface is implemented by an application to receive a notification when display attribute information is updated. This advise sink is installed by calling the TSF manager's <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfDisplayAttributeNotifySink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDisplayAttributeNotifySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfDisplayAttributeNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDisplayAttributeNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f4cbdca-b2a3-4e14-b4fb-ac65f3cec646">OnUpdateInfo</a>
</td>
<td align="left" width="63%">
Called when display attribute information is updated.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 


---
UID: NN:msctf.ITfLanguageProfileNotifySink
title: ITfLanguageProfileNotifySink
author: windows-sdk-content
description: The ITfLanguageProfileNotifySink interface is implemented by an application to receive notifications when the language profile changes.
old-location: tsf\itflanguageprofilenotifysink.htm
tech.root: TSF
ms.assetid: c0c8d02a-cc3f-4c1c-96e9-516f49b868e6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfLanguageProfileNotifySink, ITfLanguageProfileNotifySink interface [Text Services Framework], ITfLanguageProfileNotifySink interface [Text Services Framework],described, _tsf_itflanguageprofilenotifysink_ref, msctf/ITfLanguageProfileNotifySink, tsf.itflanguageprofilenotifysink
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
 - ITfLanguageProfileNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLanguageProfileNotifySink interface


## -description


The <b>ITfLanguageProfileNotifySink</b> interface is implemented by an application to receive notifications when the language profile changes.

To install this advise sink, obtain an <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> object from an <a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a> object by calling <b>ITfInputProcessorProfiles::QueryInterface</b> with <b>IID_ITfSource</b>. Then call <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with <b>IID_ITfLanguageProfileNotifySink</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLanguageProfileNotifySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLanguageProfileNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLanguageProfileNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4367265b-892b-4f75-af23-e90327fb4144">OnLanguageChange</a>
</td>
<td align="left" width="63%">
Called when the language profile is about to change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/505b3353-90cc-4b78-90af-b0151abc703f">OnLanguageChanged</a>
</td>
<td align="left" width="63%">
Called after the language profile has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles
      </a>



<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 


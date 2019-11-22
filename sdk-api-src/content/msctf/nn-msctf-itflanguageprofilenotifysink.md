---
UID: NN:msctf.ITfLanguageProfileNotifySink
title: ITfLanguageProfileNotifySink (msctf.h)

description: The ITfLanguageProfileNotifySink interface is implemented by an application to receive notifications when the language profile changes.
old-location: tsf\itflanguageprofilenotifysink.htm
tech.root: TSF
ms.assetid: c0c8d02a-cc3f-4c1c-96e9-516f49b868e6

ms.date: 12/05/2018
ms.keywords: ITfLanguageProfileNotifySink, ITfLanguageProfileNotifySink interface [Text Services Framework], ITfLanguageProfileNotifySink interface [Text Services Framework],described, _tsf_itflanguageprofilenotifysink_ref, msctf/ITfLanguageProfileNotifySink, tsf.itflanguageprofilenotifysink
ms.topic: interface
f1_keywords: 
 - "msctf/ITfLanguageProfileNotifySink"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLanguageProfileNotifySink interface


## -description


The <b>ITfLanguageProfileNotifySink</b> interface is implemented by an application to receive notifications when the language profile changes.

To install this advise sink, obtain an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> object from an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a> object by calling <b>ITfInputProcessorProfiles::QueryInterface</b> with <b>IID_ITfSource</b>. Then call <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with <b>IID_ITfLanguageProfileNotifySink</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLanguageProfileNotifySink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLanguageProfileNotifySink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itflanguageprofilenotifysink-onlanguagechange">OnLanguageChange</a>
</td>
<td align="left" width="63%">
Called when the language profile is about to change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itflanguageprofilenotifysink-onlanguagechanged">OnLanguageChanged</a>
</td>
<td align="left" width="63%">
Called after the language profile has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 


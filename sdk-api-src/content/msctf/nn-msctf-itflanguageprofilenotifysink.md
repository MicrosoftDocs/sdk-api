---
UID: NN:msctf.ITfLanguageProfileNotifySink
title: ITfLanguageProfileNotifySink (msctf.h)
description: The ITfLanguageProfileNotifySink interface is implemented by an application to receive notifications when the language profile changes.
helpviewer_keywords: ["ITfLanguageProfileNotifySink","ITfLanguageProfileNotifySink interface [Text Services Framework]","ITfLanguageProfileNotifySink interface [Text Services Framework]","described","_tsf_itflanguageprofilenotifysink_ref","msctf/ITfLanguageProfileNotifySink","tsf.itflanguageprofilenotifysink"]
old-location: tsf\itflanguageprofilenotifysink.htm
tech.root: TSF
ms.assetid: c0c8d02a-cc3f-4c1c-96e9-516f49b868e6
ms.date: 12/05/2018
ms.keywords: ITfLanguageProfileNotifySink, ITfLanguageProfileNotifySink interface [Text Services Framework], ITfLanguageProfileNotifySink interface [Text Services Framework],described, _tsf_itflanguageprofilenotifysink_ref, msctf/ITfLanguageProfileNotifySink, tsf.itflanguageprofilenotifysink
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfLanguageProfileNotifySink
 - msctf/ITfLanguageProfileNotifySink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLanguageProfileNotifySink
---

# ITfLanguageProfileNotifySink interface


## -description

The <b>ITfLanguageProfileNotifySink</b> interface is implemented by an application to receive notifications when the language profile changes.

To install this advise sink, obtain an <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> object from an <a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a> object by calling <b>ITfInputProcessorProfiles::QueryInterface</b> with <b>IID_ITfSource</b>. Then call <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with <b>IID_ITfLanguageProfileNotifySink</b>.

## -inheritance

The <b>ITfLanguageProfileNotifySink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLanguageProfileNotifySink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

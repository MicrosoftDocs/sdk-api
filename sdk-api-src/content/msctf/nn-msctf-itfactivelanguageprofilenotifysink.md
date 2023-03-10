---
UID: NN:msctf.ITfActiveLanguageProfileNotifySink
title: ITfActiveLanguageProfileNotifySink (msctf.h)
description: The ITfActiveLanguageProfileNotifySink interface is implemented by an application to receive a notification when the active language or text service changes.
helpviewer_keywords: ["ITfActiveLanguageProfileNotifySink","ITfActiveLanguageProfileNotifySink interface [Text Services Framework]","ITfActiveLanguageProfileNotifySink interface [Text Services Framework]","described","_tsf_itfactivelanguageprofilenotifysink_ref","msctf/ITfActiveLanguageProfileNotifySink","tsf.itfactivelanguageprofilenotifysink"]
old-location: tsf\itfactivelanguageprofilenotifysink.htm
tech.root: TSF
ms.assetid: c70141e8-c948-44f4-914e-454327aadf2b
ms.date: 12/05/2018
ms.keywords: ITfActiveLanguageProfileNotifySink, ITfActiveLanguageProfileNotifySink interface [Text Services Framework], ITfActiveLanguageProfileNotifySink interface [Text Services Framework],described, _tsf_itfactivelanguageprofilenotifysink_ref, msctf/ITfActiveLanguageProfileNotifySink, tsf.itfactivelanguageprofilenotifysink
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
req.dll: Imekrcic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfActiveLanguageProfileNotifySink
 - msctf/ITfActiveLanguageProfileNotifySink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imekrcic.dll
api_name:
 - ITfActiveLanguageProfileNotifySink
---

# ITfActiveLanguageProfileNotifySink interface


## -description

The <b>ITfActiveLanguageProfileNotifySink</b> interface is implemented by an application to receive a notification when the active language or text service changes.

To install the advise sink, obtain an <a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> object from an <a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a> object by calling <b>ITfThreadMgr::QueryInterface</b> with IID_ITfActiveLanguageProfileNotifySink. Then call <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with IID_ITfActiveLanguageProfileNotifySink.

## -inheritance

The <b>ITfActiveLanguageProfileNotifySink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfActiveLanguageProfileNotifySink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

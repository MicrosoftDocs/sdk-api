---
UID: NN:ctfutb.ITfLangBarItemSink
title: ITfLangBarItemSink (ctfutb.h)
description: The ITfLangBarItemSink interface is implemented by the language bar and used by a language bar item provider to notify the language bar of changes to a language bar item.
helpviewer_keywords: ["ITfLangBarItemSink","ITfLangBarItemSink interface [Text Services Framework]","ITfLangBarItemSink interface [Text Services Framework]","described","_tsf_itflangbaritemsink_ref","ctfutb/ITfLangBarItemSink","tsf.itflangbaritemsink"]
old-location: tsf\itflangbaritemsink.htm
tech.root: TSF
ms.assetid: 1734a011-1ee8-4afd-ace8-334eeaf14518
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemSink, ITfLangBarItemSink interface [Text Services Framework], ITfLangBarItemSink interface [Text Services Framework],described, _tsf_itflangbaritemsink_ref, ctfutb/ITfLangBarItemSink, tsf.itflangbaritemsink
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - ITfLangBarItemSink
 - ctfutb/ITfLangBarItemSink
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
 - ITfLangBarItemSink
---

# ITfLangBarItemSink interface


## -description

The <b>ITfLangBarItemSink</b> interface is implemented by the language bar and used by a language bar item provider to notify the language bar of changes to a language bar item.

The language bar item provider obtains an instance of this interface when the language bar calls the provider's <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a> with identifier IID_ITfLangBarItemSink.

## -inheritance

The <b>ITfLangBarItemSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

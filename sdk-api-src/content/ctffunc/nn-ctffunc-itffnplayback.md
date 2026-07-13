---
UID: NN:ctffunc.ITfFnPlayBack
title: ITfFnPlayBack (ctffunc.h)
description: The ITfFnPlayBack interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to control the audio data for speech input text.
helpviewer_keywords: ["ITfFnPlayBack","ITfFnPlayBack interface [Text Services Framework]","ITfFnPlayBack interface [Text Services Framework]","described","_tsf_itffnplayback_ref","ctffunc/ITfFnPlayBack","tsf.itffnplayback"]
old-location: tsf\itffnplayback.htm
tech.root: TSF
ms.assetid: e9a0d1a3-70c9-4816-8cd4-f2574392953e
ms.date: 12/05/2018
ms.keywords: ITfFnPlayBack, ITfFnPlayBack interface [Text Services Framework], ITfFnPlayBack interface [Text Services Framework],described, _tsf_itffnplayback_ref, ctffunc/ITfFnPlayBack, tsf.itffnplayback
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnPlayBack
 - ctffunc/ITfFnPlayBack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnPlayBack
---

# ITfFnPlayBack interface


## -description

The <b>ITfFnPlayBack</b> interface is implemented by the Speech API (SAPI) text service. This interface is used by the TSF manager or a client (application or other text service) to control the audio data for speech input text.

Each spoken word or phrase has audio data stored with the text. This interface is used to obtain the range that covers the spoken text and to play back the audio data.

A client obtains an instance of this interface by obtaining the <a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> for the SAPI text service and calling <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> with IID_ITfFnPlayBack.

## -inheritance

The <b>ITfFnPlayBack</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnPlayBack</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

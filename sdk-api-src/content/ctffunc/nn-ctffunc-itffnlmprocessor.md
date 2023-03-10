---
UID: NN:ctffunc.ITfFnLMProcessor
title: ITfFnLMProcessor (ctffunc.h)
description: The ITfFnLMProcessor interface is implemented by the language model text service and is used by an application or text service to enable alternate language model processing.
helpviewer_keywords: ["ITfFnLMProcessor","ITfFnLMProcessor interface [Text Services Framework]","ITfFnLMProcessor interface [Text Services Framework]","described","_tsf_itffnlmprocessor_ref","ctffunc/ITfFnLMProcessor","tsf.itffnlmprocessor"]
old-location: tsf\itffnlmprocessor.htm
tech.root: TSF
ms.assetid: 89581a75-9263-45d7-99de-b3bd78a5169c
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor, ITfFnLMProcessor interface [Text Services Framework], ITfFnLMProcessor interface [Text Services Framework],described, _tsf_itffnlmprocessor_ref, ctffunc/ITfFnLMProcessor, tsf.itffnlmprocessor
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
 - ITfFnLMProcessor
 - ctffunc/ITfFnLMProcessor
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
 - ITfFnLMProcessor
---

# ITfFnLMProcessor interface


## -description

The <b>ITfFnLMProcessor</b> interface is implemented by the language model text service and is used by an application or text service to enable alternate language model processing.

The application or text service obtains this interface from a thread manager object by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">ITfThreadMgr::GetFunctionProvider</a> with GUID_MASTERLM_FUNCTIONPROVIDER and then calling <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> interface with IID_ITfFnLMProcessor. If <b>ITfThreadMgr::GetFunctionProvider</b> fails, then no language model processor is installed.

## -inheritance

The <b>ITfFnLMProcessor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnLMProcessor</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatelist">ITfCandidateList
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">ITfThreadMgr::GetFunctionProvider</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

---
UID: NN:ctffunc.ITfFnSearchCandidateProvider
title: ITfFnSearchCandidateProvider (ctffunc.h)
description: Enables an integrated search experience in an Input Method Editor (IME).
helpviewer_keywords: ["ITfFnSearchCandidateProvider","ITfFnSearchCandidateProvider interface [Text Services Framework]","ITfFnSearchCandidateProvider interface [Text Services Framework]","described","ctffunc/ITfFnSearchCandidateProvider","tsf.itffnsearchcandidateprovider"]
old-location: tsf\itffnsearchcandidateprovider.htm
tech.root: TSF
ms.assetid: 5DD99E0A-42A2-4EA5-B24F-5C439F5D7EEF
ms.date: 12/05/2018
ms.keywords: ITfFnSearchCandidateProvider, ITfFnSearchCandidateProvider interface [Text Services Framework], ITfFnSearchCandidateProvider interface [Text Services Framework],described, ctffunc/ITfFnSearchCandidateProvider, tsf.itffnsearchcandidateprovider
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfFnSearchCandidateProvider
 - ctffunc/ITfFnSearchCandidateProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - ITfFnSearchCandidateProvider
---

# ITfFnSearchCandidateProvider interface


## -description

 Enables an integrated search experience in an Input Method Editor (IME).

## -inheritance

The <b>ITfFnSearchCandidateProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfFnSearchCandidateProvider</b> also has these types of members:

## -remarks

Implement the <b>ITfFnSearchCandidateProvider</b> interface in your Input Method Editor (IME) to enable an integrated search experience. Implementing this interface enables searches with meaningful results to begin before IME input has been completed, by providing a set of possible IME conversion candidates for a given input string.  Apps can use this interface to obtain IME conversions for a string, so the <b>ITfFnSearchCandidateProvider</b> interface, along with <a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffngetlinguisticalternates">ITfFnGetLinguisticAlternates</a>, provides a TSF-based replacement for the <a href="/windows/desktop/api/imm/nf-imm-immgetconversionlista">ImmGetConversionList</a> function.  Typically IMEs implement either <b>ITfFnGetLinguisticAlternates</b> or <b>ITfFnSearchCandidateProvider</b> (or neither).

Call <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">GetFunctionProvider</a> with the CLSID of a text service to get an <a href="/windows/desktop/api/msctf/nn-msctf-itffunctionprovider">ITfFunctionProvider</a> instance.  Use the following call to the <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> method to get the <b>ITfFnSearchCandidateProvider</b> interface pointer.

<code>ITfFunctionProvider::GetFunction(GUID_NULL, IID_ITfFnSearchCandidateProvider, &amp;pSearchCandidate)</code>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">GetFunction</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfunctionprovider">GetFunctionProvider</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/uwp/api/windows.applicationmodel.search.searchpanequerylinguisticdetails">SearchPaneQueryLinguisticDetails</a>

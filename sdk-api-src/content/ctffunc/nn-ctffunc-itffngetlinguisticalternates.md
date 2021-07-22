---
UID: NN:ctffunc.ITfFnGetLinguisticAlternates
title: ITfFnGetLinguisticAlternates (ctffunc.h)
description: The ITfFnGetLinguisticAlternates interface is implemented by a text service and/or by the TSF manager to provide linguistic alternates for the text within a given range passed as a parameter.
helpviewer_keywords: ["ITfFnGetLinguisticAlternates","ITfFnGetLinguisticAlternates interface [Text Services Framework]","ITfFnGetLinguisticAlternates interface [Text Services Framework]","described","ctffunc/ITfFnGetLinguisticAlternates","tsf.itffngetlinguisticalternates"]
old-location: tsf\itffngetlinguisticalternates.htm
tech.root: TSF
ms.assetid: 854FB6EC-CEF1-4FB6-AA5F-34B26B46A3CA
ms.date: 12/05/2018
ms.keywords: ITfFnGetLinguisticAlternates, ITfFnGetLinguisticAlternates interface [Text Services Framework], ITfFnGetLinguisticAlternates interface [Text Services Framework],described, ctffunc/ITfFnGetLinguisticAlternates, tsf.itffngetlinguisticalternates
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - ITfFnGetLinguisticAlternates
 - ctffunc/ITfFnGetLinguisticAlternates
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
 - ITfFnGetLinguisticAlternates
---

# ITfFnGetLinguisticAlternates interface


## -description

The <b>ITfFnGetLinguisticAlternates</b> interface is implemented by a text service and/or by the TSF manager to provide linguistic alternates for the text within a given range passed as a parameter.

Apps can use this interface to obtain IME alternates for a text range; therefore the interface <b>ITfFnGetLinguisticAlternates</b>, along with <a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnsearchcandidateprovider">ITfFnSearchCandidateProvider</a>, provides a TSF-based replacement for the <a href="/windows/desktop/api/imm/nf-imm-immgetconversionlista">ImmGetConversionList</a> function.  Typically IMEs implement either <b>ITfFnGetLinguisticAlternates</b> or <b>ITfFnSearchCandidateProvider</b> (or neither).

An app obtains a pointer to this interface by calling TSF manager <a href="/windows/desktop/api/msctf/nf-msctf-itffunctionprovider-getfunction">ITfFunctionProvider::GetFunction</a> method with <b>IID_ITfFnGetLinguisticAlternates</b>.


<div class="alert"><b>Note</b>  This interface may not be supported for all IMEs. There may be differences in support between IMEs on the Desktop and IMEs in the new Windows UI on Windows 8.1.  Some IMEs instead implement the related interface <a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnsearchcandidateprovider">ITfFnSearchCandidateProvider</a> that can be used as a substitute for this API.  Suggested app usage is to check for this interface first, and if it's not available then check if <b>ITfFnSearchCandidateProvider</b> is supported instead.  IMEs that wish to maintain compatibility with Windows 8 should implement <b>ITfFnSearchCandidateProvider</b> instead.</div>
<div> </div>

## -inheritance

The <b>ITfFnGetLinguisticAlternates</b> interface inherits from <a href="/windows/desktop/api/msctf/nn-msctf-itffunction">ITfFunction</a>. <b>ITfFnGetLinguisticAlternates</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itffunction">ITfFunction</a>

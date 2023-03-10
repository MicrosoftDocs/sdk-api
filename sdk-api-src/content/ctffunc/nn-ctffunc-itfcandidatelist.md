---
UID: NN:ctffunc.ITfCandidateList
title: ITfCandidateList (ctffunc.h)
description: The ITfCandidateList interface is implemented by a text service and is used by the TSF manager or a client (application or other text service) to obtain and manipulate candidate string objects.
helpviewer_keywords: ["ITfCandidateList","ITfCandidateList interface [Text Services Framework]","ITfCandidateList interface [Text Services Framework]","described","_tsf_itfcandidatelist_ref","ctffunc/ITfCandidateList","tsf.itfcandidatelist"]
old-location: tsf\itfcandidatelist.htm
tech.root: TSF
ms.assetid: e41ba461-6337-4feb-ba16-3942920ebb9f
ms.date: 12/05/2018
ms.keywords: ITfCandidateList, ITfCandidateList interface [Text Services Framework], ITfCandidateList interface [Text Services Framework],described, _tsf_itfcandidatelist_ref, ctffunc/ITfCandidateList, tsf.itfcandidatelist
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCandidateList
 - ctffunc/ITfCandidateList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tiptsf.dll
api_name:
 - ITfCandidateList
---

# ITfCandidateList interface


## -description

The <b>ITfCandidateList</b> interface is implemented by a text service and is used by the TSF manager or a client (application or other text service) to obtain and manipulate candidate string objects.

The TSF manager implements this interface to provide access to this interface to other clients. This enables the TSF manager to function as a mediator between the client and the text service.

To obtain an instance of this interface the TSF manager or client can call <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-getreconversion">ITfFnReconversion::GetReconversion</a>.

## -inheritance

The <b>ITfCandidateList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCandidateList</b> also has these types of members:

## -remarks

When a text service must interpret text before it is inserted into a context, there might be more than one possible interpretation of the text. Speech input is an example of this. If the spoken word is "there", other possible interpretations might be "their" or "they're". The text service will insert the most appropriate text, but there is still some chance of error involved. Text reconversion is the process of allowing the user to select alternate text for the inserted text. The alternate text objects are known as candidates.

## -see-also

<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnreconversion-getreconversion">ITfFnReconversion::GetReconversion
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

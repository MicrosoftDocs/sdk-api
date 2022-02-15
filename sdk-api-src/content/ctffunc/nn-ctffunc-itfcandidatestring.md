---
UID: NN:ctffunc.ITfCandidateString
title: ITfCandidateString (ctffunc.h)
description: The ITfCandidateString interface is implemented by a text service and is used by the TSF manager or a client to obtain information about a candidate string object.
helpviewer_keywords: ["ITfCandidateString","ITfCandidateString interface [Text Services Framework]","ITfCandidateString interface [Text Services Framework]","described","_tsf_itfcandidatestring_ref","ctffunc/ITfCandidateString","tsf.itfcandidatestring"]
old-location: tsf\itfcandidatestring.htm
tech.root: TSF
ms.assetid: 82c77b59-a50c-42ae-ba1d-25a1c196662d
ms.date: 12/05/2018
ms.keywords: ITfCandidateString, ITfCandidateString interface [Text Services Framework], ITfCandidateString interface [Text Services Framework],described, _tsf_itfcandidatestring_ref, ctffunc/ITfCandidateString, tsf.itfcandidatestring
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
 - ITfCandidateString
 - ctffunc/ITfCandidateString
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
 - ITfCandidateString
---

# ITfCandidateString interface


## -description

The <b>ITfCandidateString</b> interface is implemented by a text service and is used by the TSF manager or a client to obtain information about a candidate string object.

The TSF manager implements this interface to provide access to this interface to other clients. This enables the TSF manager to function as a mediator between the client and the text service.

To obtain an instance of this interface, the TSF manager or client can call <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-getcandidate">ITfCandidateList::GetCandidate</a>.

## -inheritance

The <b>ITfCandidateString</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfCandidateString</b> also has these types of members:


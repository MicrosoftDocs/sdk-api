---
UID: NE:ctffunc.__MIDL_ITfCandidateList_0001
title: TfCandidateResult (ctffunc.h)
description: Elements of the TfCandidateResult enumeration are used with the ITfCandidateList::SetResult method to specify the result of a reconversion operation performed on a given candidate string.
helpviewer_keywords: ["CAND_CANCELED","CAND_FINALIZED","CAND_SELECTED","TfCandidateResult","TfCandidateResult enumeration [Text Services Framework]","_tsf_tfcandidateresult_ref","ctffunc/CAND_CANCELED","ctffunc/CAND_FINALIZED","ctffunc/CAND_SELECTED","ctffunc/TfCandidateResult","tsf.tfcandidateresult"]
old-location: tsf\tfcandidateresult.htm
tech.root: TSF
ms.assetid: 8b2b4762-f28d-40e0-b162-5e35e8835c8e
ms.date: 12/05/2018
ms.keywords: CAND_CANCELED, CAND_FINALIZED, CAND_SELECTED, TfCandidateResult, TfCandidateResult enumeration [Text Services Framework], _tsf_tfcandidateresult_ref, ctffunc/CAND_CANCELED, ctffunc/CAND_FINALIZED, ctffunc/CAND_SELECTED, ctffunc/TfCandidateResult, tsf.tfcandidateresult
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TfCandidateResult
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - __MIDL_ITfCandidateList_0001
 - ctffunc/__MIDL_ITfCandidateList_0001
 - TfCandidateResult
 - ctffunc/TfCandidateResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ctffunc.h
api_name:
 - TfCandidateResult
---

# TfCandidateResult enumeration


## -description

Elements of the <b>TfCandidateResult</b> enumeration are used with the <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-setresult">ITfCandidateList::SetResult</a> method to specify the result of a reconversion operation performed on a given candidate string.

## -enum-fields

### -field CAND_FINALIZED:0

The candidate string has been selected and accepted. The previous text should be replaced with the specified candidate.

### -field CAND_SELECTED:0x1

The candidate string has been selected, but the selection is not yet final.

### -field CAND_CANCELED:0x2

The reconversion operation has been canceled.

## -see-also

<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itfcandidatelist-setresult">ITfCandidateList::SetResult
      </a>

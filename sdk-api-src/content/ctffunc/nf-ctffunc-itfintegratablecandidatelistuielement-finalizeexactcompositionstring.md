---
UID: NF:ctffunc.ITfIntegratableCandidateListUIElement.FinalizeExactCompositionString
title: ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString (ctffunc.h)
description: Finalizes the current composition with the value currently shown to the user.
helpviewer_keywords: ["FinalizeExactCompositionString","FinalizeExactCompositionString method [Text Services Framework]","FinalizeExactCompositionString method [Text Services Framework]","ITfIntegratableCandidateListUIElement interface","ITfIntegratableCandidateListUIElement interface [Text Services Framework]","FinalizeExactCompositionString method","ITfIntegratableCandidateListUIElement.FinalizeExactCompositionString","ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString","ctffunc/ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString","tsf.itfintegratablecandidatelistuielement_finalizeexactcompositionstring"]
old-location: tsf\itfintegratablecandidatelistuielement_finalizeexactcompositionstring.htm
tech.root: TSF
ms.assetid: 1A81C1D7-2D7A-41A0-9DB7-0F30AE610051
ms.date: 12/05/2018
ms.keywords: FinalizeExactCompositionString, FinalizeExactCompositionString method [Text Services Framework], FinalizeExactCompositionString method [Text Services Framework],ITfIntegratableCandidateListUIElement interface, ITfIntegratableCandidateListUIElement interface [Text Services Framework],FinalizeExactCompositionString method, ITfIntegratableCandidateListUIElement.FinalizeExactCompositionString, ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString, ctffunc/ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString, tsf.itfintegratablecandidatelistuielement_finalizeexactcompositionstring
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
 - ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString
 - ctffunc/ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString
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
 - ITfIntegratableCandidateListUIElement.FinalizeExactCompositionString
---

# ITfIntegratableCandidateListUIElement::FinalizeExactCompositionString


## -description

Finalizes the current composition with the value currently shown to the user.



## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -remarks

The <b>FinalizeExactCompositionString</b> method enables an app to tell the text service that it should finalize the current composition with the exact
    value currently shown to the user, with no automatic conversion of the first candidate.  This enables the apps to move focus
    to suggestions below the candidate list, without changing the string.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfintegratablecandidatelistuielement">ITfIntegratableCandidateListUIElement</a>

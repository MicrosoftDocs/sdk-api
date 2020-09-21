---
UID: NF:ctffunc.ITfIntegratableCandidateListUIElement.GetSelectionStyle
title: ITfIntegratableCandidateListUIElement::GetSelectionStyle (ctffunc.h)
description: Retrieves the selection style.
helpviewer_keywords: ["GetSelectionStyle","GetSelectionStyle method [Text Services Framework]","GetSelectionStyle method [Text Services Framework]","ITfIntegratableCandidateListUIElement interface","ITfIntegratableCandidateListUIElement interface [Text Services Framework]","GetSelectionStyle method","ITfIntegratableCandidateListUIElement.GetSelectionStyle","ITfIntegratableCandidateListUIElement::GetSelectionStyle","ctffunc/ITfIntegratableCandidateListUIElement::GetSelectionStyle","tsf.itfintegratablecandidatelistuielement_getselectionstyle"]
old-location: tsf\itfintegratablecandidatelistuielement_getselectionstyle.htm
tech.root: TSF
ms.assetid: D51E27FE-503E-459C-92F1-1826762A5188
ms.date: 12/05/2018
ms.keywords: GetSelectionStyle, GetSelectionStyle method [Text Services Framework], GetSelectionStyle method [Text Services Framework],ITfIntegratableCandidateListUIElement interface, ITfIntegratableCandidateListUIElement interface [Text Services Framework],GetSelectionStyle method, ITfIntegratableCandidateListUIElement.GetSelectionStyle, ITfIntegratableCandidateListUIElement::GetSelectionStyle, ctffunc/ITfIntegratableCandidateListUIElement::GetSelectionStyle, tsf.itfintegratablecandidatelistuielement_getselectionstyle
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
 - ITfIntegratableCandidateListUIElement::GetSelectionStyle
 - ctffunc/ITfIntegratableCandidateListUIElement::GetSelectionStyle
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
 - ITfIntegratableCandidateListUIElement.GetSelectionStyle
---

# ITfIntegratableCandidateListUIElement::GetSelectionStyle


## -description

Retrieves the selection style.

## -parameters

### -param ptfSelectionStyle [out]

A value that specifies the selection style.

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

The active selection style usually indicates that the selection can be changed with the arrow keys. The implied selection style indicates the default selection key chooses it.
         If the app supports changing selection styles, this method should be called when the <a href="/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-updateuielement">UpdateUIElement</a> method is called.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfintegratablecandidatelistuielement">ITfIntegratableCandidateListUIElement</a>
---
UID: NF:ctffunc.ITfFnLMProcessor.QueryLangID
title: ITfFnLMProcessor::QueryLangID (ctffunc.h)
description: ITfFnLMProcessor::QueryLangID method
helpviewer_keywords: ["ITfFnLMProcessor interface [Text Services Framework]","QueryLangID method","ITfFnLMProcessor.QueryLangID","ITfFnLMProcessor::QueryLangID","QueryLangID","QueryLangID method [Text Services Framework]","QueryLangID method [Text Services Framework]","ITfFnLMProcessor interface","_tsf_itffnlmprocessor_querylangid_ref","ctffunc/ITfFnLMProcessor::QueryLangID","tsf.itffnlmprocessor_querylangid"]
old-location: tsf\itffnlmprocessor_querylangid.htm
tech.root: TSF
ms.assetid: 2d645c1b-9ee6-47c4-8bbd-173e416f5688
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],QueryLangID method, ITfFnLMProcessor.QueryLangID, ITfFnLMProcessor::QueryLangID, QueryLangID, QueryLangID method [Text Services Framework], QueryLangID method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_querylangid_ref, ctffunc/ITfFnLMProcessor::QueryLangID, tsf.itffnlmprocessor_querylangid
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
 - ITfFnLMProcessor::QueryLangID
 - ctffunc/ITfFnLMProcessor::QueryLangID
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
 - ITfFnLMProcessor.QueryLangID
---

# ITfFnLMProcessor::QueryLangID


## -description

Determines if the language model text service supports a particular language.

## -parameters

### -param langid [in]

Contains a <b>LANGID</b> that specifies the identifier of the language that the query applies to.

### -param pfAccepted [out]

Pointer to a <b>BOOL</b> value that receives nonzero if the language model text service supports the language identified by <i>langid</i> or zero otherwise.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfAccepted</i> is invalid.

</td>
</tr>
</table>

## -remarks

If a client can possibly generate more than one language identifier of text, it should query all with this method.


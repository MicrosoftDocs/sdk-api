---
UID: NF:ctffunc.ITfFnLMProcessor.QueryLangID
title: ITfFnLMProcessor::QueryLangID method
author: windows-driver-content
description: ITfFnLMProcessor::QueryLangID method
old-location: tsf\itffnlmprocessor_querylangid.htm
old-project: TSF
ms.assetid: 2d645c1b-9ee6-47c4-8bbd-173e416f5688
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfFnLMProcessor, ITfFnLMProcessor interface [Text Services Framework], QueryLangID method, ITfFnLMProcessor::QueryLangID, QueryLangID method [Text Services Framework], QueryLangID method [Text Services Framework], ITfFnLMProcessor interface, QueryLangID,ITfFnLMProcessor.QueryLangID, _tsf_itffnlmprocessor_querylangid_ref, ctffunc/ITfFnLMProcessor::QueryLangID, tsf.itffnlmprocessor_querylangid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfFnLMProcessor.QueryLangID
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnLMProcessor::QueryLangID method


## -description




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




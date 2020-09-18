---
UID: NF:ctffunc.ITfFnLMProcessor.QueryKey
title: ITfFnLMProcessor::QueryKey (ctffunc.h)
description: ITfFnLMProcessor::QueryKey method
helpviewer_keywords: ["ITfFnLMProcessor interface [Text Services Framework]","QueryKey method","ITfFnLMProcessor.QueryKey","ITfFnLMProcessor::QueryKey","QueryKey","QueryKey method [Text Services Framework]","QueryKey method [Text Services Framework]","ITfFnLMProcessor interface","_tsf_itffnlmprocessor_querykey_ref","ctffunc/ITfFnLMProcessor::QueryKey","tsf.itffnlmprocessor_querykey"]
old-location: tsf\itffnlmprocessor_querykey.htm
tech.root: TSF
ms.assetid: 9d28c2c2-ed0e-4987-ace9-25ed9d7a40a0
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],QueryKey method, ITfFnLMProcessor.QueryKey, ITfFnLMProcessor::QueryKey, QueryKey, QueryKey method [Text Services Framework], QueryKey method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_querykey_ref, ctffunc/ITfFnLMProcessor::QueryKey, tsf.itffnlmprocessor_querykey
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
 - ITfFnLMProcessor::QueryKey
 - ctffunc/ITfFnLMProcessor::QueryKey
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
 - ITfFnLMProcessor.QueryKey
---

# ITfFnLMProcessor::QueryKey


## -description

Called to determine if the language model text service handles a key event.

## -parameters

### -param fUp [in]

Contains a <b>BOOL</b> that specifies if this is a key-down or a key-up event. Contains zero if this is a key-down event or nonzero otherwise.

### -param vKey [in]

Contains the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param lparamKeydata [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param pfInterested [out]

Pointer to a <b>BOOL</b> that receives nonzero if the language model text service will handle the key event or zero otherwise.

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

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnlmprocessor">ITfFnLMProcessor</a>



<a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>



<a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a>
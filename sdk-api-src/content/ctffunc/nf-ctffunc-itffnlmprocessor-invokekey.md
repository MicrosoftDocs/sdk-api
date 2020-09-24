---
UID: NF:ctffunc.ITfFnLMProcessor.InvokeKey
title: ITfFnLMProcessor::InvokeKey (ctffunc.h)
description: ITfFnLMProcessor::InvokeKey method
helpviewer_keywords: ["ITfFnLMProcessor interface [Text Services Framework]","InvokeKey method","ITfFnLMProcessor.InvokeKey","ITfFnLMProcessor::InvokeKey","InvokeKey","InvokeKey method [Text Services Framework]","InvokeKey method [Text Services Framework]","ITfFnLMProcessor interface","_tsf_itffnlmprocessor_invokekey_ref","ctffunc/ITfFnLMProcessor::InvokeKey","tsf.itffnlmprocessor_invokekey"]
old-location: tsf\itffnlmprocessor_invokekey.htm
tech.root: TSF
ms.assetid: 0611dd1e-6f79-4397-b523-e4fb278725f7
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],InvokeKey method, ITfFnLMProcessor.InvokeKey, ITfFnLMProcessor::InvokeKey, InvokeKey, InvokeKey method [Text Services Framework], InvokeKey method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_invokekey_ref, ctffunc/ITfFnLMProcessor::InvokeKey, tsf.itffnlmprocessor_invokekey
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
 - ITfFnLMProcessor::InvokeKey
 - ctffunc/ITfFnLMProcessor::InvokeKey
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
 - ITfFnLMProcessor.InvokeKey
---

# ITfFnLMProcessor::InvokeKey


## -description

Called to enable the language model text service to process a key event.

## -parameters

### -param fUp [in]

Contains a <b>BOOL</b> that specifies if this is a key-down or a key-up event. Contains zero if this is a key-down event or nonzero otherwise.

### -param vKey [in]

Contains the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

### -param lparamKeyData [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>.

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
---
UID: NF:ctffunc.ITfFnLMProcessor.InvokeKey
title: ITfFnLMProcessor::InvokeKey (ctffunc.h)
author: windows-sdk-content
description: ITfFnLMProcessor::InvokeKey method
old-location: tsf\itffnlmprocessor_invokekey.htm
tech.root: TSF
ms.assetid: 0611dd1e-6f79-4397-b523-e4fb278725f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],InvokeKey method, ITfFnLMProcessor.InvokeKey, ITfFnLMProcessor::InvokeKey, InvokeKey, InvokeKey method [Text Services Framework], InvokeKey method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_invokekey_ref, ctffunc/ITfFnLMProcessor::InvokeKey, tsf.itffnlmprocessor_invokekey
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnLMProcessor.InvokeKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnLMProcessor::InvokeKey


## -description




## -parameters




### -param fUp [in]

Contains a <b>BOOL</b> that specifies if this is a key-down or a key-up event. Contains zero if this is a key-down event or nonzero otherwise.


### -param vKey [in]

Contains the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>.


### -param lparamKeyData [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>.


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




<a href="https://msdn.microsoft.com/89581a75-9263-45d7-99de-b3bd78a5169c">ITfFnLMProcessor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>
 

 


---
UID: NF:ctffunc.ITfFnLMProcessor.QueryKey
title: ITfFnLMProcessor::QueryKey
author: windows-sdk-content
description: ITfFnLMProcessor::QueryKey method
old-location: tsf\itffnlmprocessor_querykey.htm
old-project: TSF
ms.assetid: 9d28c2c2-ed0e-4987-ace9-25ed9d7a40a0
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITfFnLMProcessor interface [Text Services Framework],QueryKey method, ITfFnLMProcessor.QueryKey, ITfFnLMProcessor::QueryKey, QueryKey, QueryKey method [Text Services Framework], QueryKey method [Text Services Framework],ITfFnLMProcessor interface, _tsf_itffnlmprocessor_querykey_ref, ctffunc/ITfFnLMProcessor::QueryKey, tsf.itffnlmprocessor_querykey
ms.prod: windows
ms.technology: windows-sdk
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
-	ITfFnLMProcessor.QueryKey
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnLMProcessor::QueryKey


## -description




## -parameters




### -param fUp [in]

Contains a <b>BOOL</b> that specifies if this is a key-down or a key-up event. Contains zero if this is a key-down event or nonzero otherwise.


### -param vKey [in]

Contains the virtual-key code of the key. For more information about this parameter, see the <i>wParam</i> parameter in <a href="_win32_wm_keydown">WM_KEYDOWN</a>.


### -param lparamKeydata [in]

Specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag of the key. For more information about this parameter, see the <i>lParam</i> parameter in <a href="_win32_wm_keydown">WM_KEYDOWN</a>.


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




<a href="https://msdn.microsoft.com/89581a75-9263-45d7-99de-b3bd78a5169c">ITfFnLMProcessor</a>



<a href="_win32_wm_keydown">WM_KEYDOWN</a>



<a href="_win32_wm_keyup">WM_KEYUP</a>
 

 


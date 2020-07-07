---
UID: NS:dpapi._CRYPTPROTECT_PROMPTSTRUCT
title: CRYPTPROTECT_PROMPTSTRUCT (dpapi.h)
description: Provides the text of a prompt and information about when and where that prompt is to be displayed when using the CryptProtectData and CryptUnprotectData functions.
helpviewer_keywords: ["*PCRYPTPROTECT_PROMPTSTRUCT","CRYPTPROTECT_PROMPTSTRUCT","CRYPTPROTECT_PROMPTSTRUCT structure [Security]","CRYPTPROTECT_PROMPT_ON_PROTECT","CRYPTPROTECT_PROMPT_ON_UNPROTECT","PCRYPTPROTECT_PROMPTSTRUCT","PCRYPTPROTECT_PROMPTSTRUCT structure pointer [Security]","_crypto2_cryptprotect_promptstruct","dpapi/CRYPTPROTECT_PROMPTSTRUCT","dpapi/PCRYPTPROTECT_PROMPTSTRUCT","security.cryptprotect_promptstruct","wincrypt/CRYPTPROTECT_PROMPTSTRUCT","wincrypt/PCRYPTPROTECT_PROMPTSTRUCT"]
old-location: security\cryptprotect_promptstruct.htm
tech.root: SecCrypto
ms.assetid: 412ce598-a7c9-446d-bd98-6583a20d6cd7
ms.date: 12/05/2018
ms.keywords: '*PCRYPTPROTECT_PROMPTSTRUCT, CRYPTPROTECT_PROMPTSTRUCT, CRYPTPROTECT_PROMPTSTRUCT structure [Security], CRYPTPROTECT_PROMPT_ON_PROTECT, CRYPTPROTECT_PROMPT_ON_UNPROTECT, PCRYPTPROTECT_PROMPTSTRUCT, PCRYPTPROTECT_PROMPTSTRUCT structure pointer [Security], _crypto2_cryptprotect_promptstruct, dpapi/CRYPTPROTECT_PROMPTSTRUCT, dpapi/PCRYPTPROTECT_PROMPTSTRUCT, security.cryptprotect_promptstruct, wincrypt/CRYPTPROTECT_PROMPTSTRUCT, wincrypt/PCRYPTPROTECT_PROMPTSTRUCT'
f1_keywords:
- dpapi/CRYPTPROTECT_PROMPTSTRUCT
dev_langs:
- c++
req.header: dpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Dpapi.h
- Wincrypt.h
api_name:
- CRYPTPROTECT_PROMPTSTRUCT
targetos: Windows
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
req.redist: 
ms.custom: 19H1
---

# CRYPTPROTECT_PROMPTSTRUCT structure


## -description


The <b>CRYPTPROTECT_PROMPTSTRUCT</b> structure provides the text of a prompt and information about when and where that prompt is to be displayed when using the 
<a href="https://docs.microsoft.com/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata">CryptUnprotectData</a> functions.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field dwPromptFlags

<b>DWORD</b> flags that indicate when prompts to the user are to be displayed. Current <b>dwPromptFlags</b> values are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_PROMPT_ON_PROTECT"></a><a id="cryptprotect_prompt_on_protect"></a><dl>
<dt><b>CRYPTPROTECT_PROMPT_ON_PROTECT</b></dt>
</dl>
</td>
<td width="60%">
This flag is used to provide the prompt for the protect phase.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_PROMPT_ON_UNPROTECT"></a><a id="cryptprotect_prompt_on_unprotect"></a><dl>
<dt><b>CRYPTPROTECT_PROMPT_ON_UNPROTECT</b></dt>
</dl>
</td>
<td width="60%">
This flag can be combined with CRYPTPROTECT_PROMPT_ON_PROTECT to enforce the UI (user interface) policy of the caller. When <a href="https://docs.microsoft.com/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata">CryptUnprotectData</a> is called, the <b>dwPromptFlags</b> specified in the <a href="https://docs.microsoft.com/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a> call are enforced.

</td>
</tr>
</table>
 


### -field hwndApp

Window handle to the parent window.


### -field szPrompt

A string containing the text of a prompt to be displayed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata">CryptUnprotectData</a>
 

 


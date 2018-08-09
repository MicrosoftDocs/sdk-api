---
UID: NS:dpapi._CRYPTPROTECT_PROMPTSTRUCT
title: "_CRYPTPROTECT_PROMPTSTRUCT"
author: windows-sdk-content
description: Provides the text of a prompt and information about when and where that prompt is to be displayed when using the CryptProtectData and CryptUnprotectData functions.
old-location: security\cryptprotect_promptstruct.htm
old-project: seccrypto
ms.assetid: 412ce598-a7c9-446d-bd98-6583a20d6cd7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCRYPTPROTECT_PROMPTSTRUCT, CRYPTPROTECT_PROMPTSTRUCT, CRYPTPROTECT_PROMPTSTRUCT structure [Security], CRYPTPROTECT_PROMPT_ON_PROTECT, CRYPTPROTECT_PROMPT_ON_UNPROTECT, PCRYPTPROTECT_PROMPTSTRUCT, PCRYPTPROTECT_PROMPTSTRUCT structure pointer [Security], _CRYPTPROTECT_PROMPTSTRUCT, _crypto2_cryptprotect_promptstruct, dpapi/CRYPTPROTECT_PROMPTSTRUCT, dpapi/PCRYPTPROTECT_PROMPTSTRUCT, security.cryptprotect_promptstruct, wincrypt/CRYPTPROTECT_PROMPTSTRUCT, wincrypt/PCRYPTPROTECT_PROMPTSTRUCT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CRYPTPROTECT_PROMPTSTRUCT, *PCRYPTPROTECT_PROMPTSTRUCT
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CRYPTPROTECT_PROMPTSTRUCT structure


## -description


The <b>CRYPTPROTECT_PROMPTSTRUCT</b> structure provides the text of a prompt and information about when and where that prompt is to be displayed when using the 
<a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a> and 
<a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a> functions.


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
This flag can be combined with CRYPTPROTECT_PROMPT_ON_PROTECT to enforce the UI (user interface) policy of the caller. When <a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a> is called, the <b>dwPromptFlags</b> specified in the <a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a> call are enforced.

</td>
</tr>
</table>
 


### -field hwndApp

Window handle to the parent window.


### -field szPrompt

A string containing the text of a prompt to be displayed.


## -see-also




<a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a>



<a href="https://msdn.microsoft.com/54eab3b0-d341-47c6-9c32-79328d7a7155">CryptUnprotectData</a>
 

 


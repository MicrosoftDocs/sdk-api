---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


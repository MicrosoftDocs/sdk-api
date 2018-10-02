---
UID: NE:msxml6._XHR_CRED_PROMPT
title: "_XHR_CRED_PROMPT"
author: windows-sdk-content
description: Specifies whether to allow credential prompts to the user for authentication.
old-location: ixhr2\xhr_cred_prompt.htm
tech.root: ixhr2
ms.assetid: 01160bda-0d4c-46fc-92ba-82fe5808e665
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: XHR_CRED_PROMPT, XHR_CRED_PROMPT enumeration [XMLHttpRequest2], XHR_CRED_PROMPT_ALL, XHR_CRED_PROMPT_NONE, XHR_CRED_PROMPT_PROXY, _XHR_CRED_PROMPT, ixhr2.xhr_cred_prompt, msxml6/XHR_CRED_PROMPT, msxml6/XHR_CRED_PROMPT_ALL, msxml6/XHR_CRED_PROMPT_NONE, msxml6/XHR_CRED_PROMPT_PROXY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - msxml6.h
api_name:
 - XHR_CRED_PROMPT
product: Windows
targetos: Windows
req.typenames: XHR_CRED_PROMPT
req.redist: 
---

# _XHR_CRED_PROMPT enumeration


## -description


Specifies whether to allow credential prompts to the user for authentication. 


## -enum-fields




### -field XHR_CRED_PROMPT_ALL

Allow all credential prompts for authentication. 

This setting allows credential prompts in response to requests from the proxy or the server.


### -field XHR_CRED_PROMPT_NONE

Disable all credential prompts for authentication. This setting disables any credential prompts in response to requests from the proxy or the server.


### -field XHR_CRED_PROMPT_PROXY

Allow credential prompts for authentication only in response to requests from the proxy.

This setting disables any credential prompts in response to requests from the server.


## -see-also




<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 


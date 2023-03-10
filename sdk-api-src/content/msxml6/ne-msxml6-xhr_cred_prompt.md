---
UID: NE:msxml6._XHR_CRED_PROMPT
title: XHR_CRED_PROMPT (msxml6.h)
description: Specifies whether to allow credential prompts to the user for authentication.
helpviewer_keywords: ["XHR_CRED_PROMPT","XHR_CRED_PROMPT enumeration [XMLHttpRequest2]","XHR_CRED_PROMPT_ALL","XHR_CRED_PROMPT_NONE","XHR_CRED_PROMPT_PROXY","ixhr2.xhr_cred_prompt","msxml6/XHR_CRED_PROMPT","msxml6/XHR_CRED_PROMPT_ALL","msxml6/XHR_CRED_PROMPT_NONE","msxml6/XHR_CRED_PROMPT_PROXY"]
old-location: ixhr2\xhr_cred_prompt.htm
tech.root: ixhr2
ms.assetid: 01160bda-0d4c-46fc-92ba-82fe5808e665
ms.date: 12/05/2018
ms.keywords: XHR_CRED_PROMPT, XHR_CRED_PROMPT enumeration [XMLHttpRequest2], XHR_CRED_PROMPT_ALL, XHR_CRED_PROMPT_NONE, XHR_CRED_PROMPT_PROXY, ixhr2.xhr_cred_prompt, msxml6/XHR_CRED_PROMPT, msxml6/XHR_CRED_PROMPT_ALL, msxml6/XHR_CRED_PROMPT_NONE, msxml6/XHR_CRED_PROMPT_PROXY
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
targetos: Windows
req.typenames: XHR_CRED_PROMPT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XHR_CRED_PROMPT
 - msxml6/_XHR_CRED_PROMPT
 - XHR_CRED_PROMPT
 - msxml6/XHR_CRED_PROMPT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msxml6.h
api_name:
 - XHR_CRED_PROMPT
---

# XHR_CRED_PROMPT enumeration


## -description

Specifies whether to allow credential prompts to the user for authentication.

## -enum-fields

### -field XHR_CRED_PROMPT_ALL:0

Allow all credential prompts for authentication. 

This setting allows credential prompts in response to requests from the proxy or the server.

### -field XHR_CRED_PROMPT_NONE:0x1

Disable all credential prompts for authentication. This setting disables any credential prompts in response to requests from the proxy or the server.

### -field XHR_CRED_PROMPT_PROXY:0x2

Allow credential prompts for authentication only in response to requests from the proxy.

This setting disables any credential prompts in response to requests from the server.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>

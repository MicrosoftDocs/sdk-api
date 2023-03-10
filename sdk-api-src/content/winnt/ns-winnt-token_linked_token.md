---
UID: NS:winnt._TOKEN_LINKED_TOKEN
title: TOKEN_LINKED_TOKEN (winnt.h)
description: Contains a handle to a token. This token is linked to the token being queried by the GetTokenInformation function or set by the SetTokenInformation function.
helpviewer_keywords: ["*PTOKEN_LINKED_TOKEN","PTOKEN_LINKED_TOKEN","PTOKEN_LINKED_TOKEN structure pointer [Security]","TOKEN_LINKED_TOKEN","TOKEN_LINKED_TOKEN structure [Security]","_TOKEN_LINKED_TOKEN","security.token_linked_token","winnt/PTOKEN_LINKED_TOKEN","winnt/TOKEN_LINKED_TOKEN"]
old-location: security\token_linked_token.htm
tech.root: security
ms.assetid: a77dd410-1074-4196-8323-ccf52ed0375a
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_LINKED_TOKEN, PTOKEN_LINKED_TOKEN, PTOKEN_LINKED_TOKEN structure pointer [Security], TOKEN_LINKED_TOKEN, TOKEN_LINKED_TOKEN structure [Security], _TOKEN_LINKED_TOKEN, security.token_linked_token, winnt/PTOKEN_LINKED_TOKEN, winnt/TOKEN_LINKED_TOKEN'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TOKEN_LINKED_TOKEN, *PTOKEN_LINKED_TOKEN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_LINKED_TOKEN
 - winnt/_TOKEN_LINKED_TOKEN
 - PTOKEN_LINKED_TOKEN
 - winnt/PTOKEN_LINKED_TOKEN
 - TOKEN_LINKED_TOKEN
 - winnt/TOKEN_LINKED_TOKEN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_LINKED_TOKEN
---

# TOKEN_LINKED_TOKEN structure


## -description

The <b>TOKEN_LINKED_TOKEN</b> structure contains a handle to a token. This token is linked to the token being queried by the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function or set by the  <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a> function.

## -struct-fields

### -field LinkedToken

A handle to the linked token.

When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.
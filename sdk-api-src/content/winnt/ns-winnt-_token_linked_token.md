---
UID: NS:winnt._TOKEN_LINKED_TOKEN
title: "_TOKEN_LINKED_TOKEN"
author: windows-sdk-content
description: Contains a handle to a token. This token is linked to the token being queried by the GetTokenInformation function or set by the SetTokenInformation function.
old-location: security\token_linked_token.htm
old-project: secauthz
ms.assetid: a77dd410-1074-4196-8323-ccf52ed0375a
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: "*PTOKEN_LINKED_TOKEN, PTOKEN_LINKED_TOKEN, PTOKEN_LINKED_TOKEN structure pointer [Security], TOKEN_LINKED_TOKEN, TOKEN_LINKED_TOKEN structure [Security], _TOKEN_LINKED_TOKEN, security.token_linked_token, winnt/PTOKEN_LINKED_TOKEN, winnt/TOKEN_LINKED_TOKEN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: TOKEN_LINKED_TOKEN, *PTOKEN_LINKED_TOKEN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_LINKED_TOKEN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _TOKEN_LINKED_TOKEN structure


## -description


The <b>TOKEN_LINKED_TOKEN</b> structure contains a handle to a token. This token is linked to the token being queried by the <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function or set by the  <a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a> function.


## -struct-fields




### -field LinkedToken

A handle to the linked token.

When you have finished using the handle, close it by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


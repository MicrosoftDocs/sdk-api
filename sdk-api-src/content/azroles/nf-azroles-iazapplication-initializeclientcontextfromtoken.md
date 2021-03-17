---
UID: NF:azroles.IAzApplication.InitializeClientContextFromToken
title: IAzApplication::InitializeClientContextFromToken (azroles.h)
description: Gets an IAzClientContext object pointer from the specified client token.
helpviewer_keywords: ["AzApplication object [Security]","InitializeClientContextFromToken method","IAzApplication interface [Security]","InitializeClientContextFromToken method","IAzApplication.InitializeClientContextFromToken","IAzApplication::InitializeClientContextFromToken","InitializeClientContextFromToken","InitializeClientContextFromToken method [Security]","InitializeClientContextFromToken method [Security]","AzApplication object","InitializeClientContextFromToken method [Security]","IAzApplication interface","azroles/IAzApplication::InitializeClientContextFromToken","security.iazapplication_initializeclientcontextfromtoken"]
old-location: security\iazapplication_initializeclientcontextfromtoken.htm
tech.root: security
ms.assetid: 0002804d-0e97-4648-8aa1-14eba09a90fa
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],InitializeClientContextFromToken method, IAzApplication interface [Security],InitializeClientContextFromToken method, IAzApplication.InitializeClientContextFromToken, IAzApplication::InitializeClientContextFromToken, InitializeClientContextFromToken, InitializeClientContextFromToken method [Security], InitializeClientContextFromToken method [Security],AzApplication object, InitializeClientContextFromToken method [Security],IAzApplication interface, azroles/IAzApplication::InitializeClientContextFromToken, security.iazapplication_initializeclientcontextfromtoken
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication::InitializeClientContextFromToken
 - azroles/IAzApplication::InitializeClientContextFromToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.InitializeClientContextFromToken
 - AzApplication.InitializeClientContextFromToken
---

# IAzApplication::InitializeClientContextFromToken


## -description

The <b>InitializeClientContextFromToken</b> method gets an <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object pointer from the specified client token.

## -parameters

### -param ullTokenHandle [in]

A handle to a Windows token that specifies the client. If this parameter is <b>NULL</b>, the impersonation token of the caller's thread is used. If the thread does not have an impersonation token, the process token is used. The token must have been opened for TOKEN_QUERY, TOKEN_IMPERSONATE, and TOKEN_DUPLICATE access.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppClientContext [out]

A pointer to a pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext">IAzClientContext</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.
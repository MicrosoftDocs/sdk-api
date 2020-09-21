---
UID: NF:azroles.IAzApplication2.InitializeClientContextFromToken2
title: IAzApplication2::InitializeClientContextFromToken2 (azroles.h)
description: Retrieves an IAzClientContext2 object pointer from the specified client token.
helpviewer_keywords: ["IAzApplication2 interface [Security]","InitializeClientContextFromToken2 method","IAzApplication2.InitializeClientContextFromToken2","IAzApplication2::InitializeClientContextFromToken2","InitializeClientContextFromToken2","InitializeClientContextFromToken2 method [Security]","InitializeClientContextFromToken2 method [Security]","IAzApplication2 interface","azroles/IAzApplication2::InitializeClientContextFromToken2","security.iazapplication2_initializeclientcontextfromtoken2"]
old-location: security\iazapplication2_initializeclientcontextfromtoken2.htm
tech.root: security
ms.assetid: f77b5eb1-c121-4392-a317-7021059268ed
ms.date: 12/05/2018
ms.keywords: IAzApplication2 interface [Security],InitializeClientContextFromToken2 method, IAzApplication2.InitializeClientContextFromToken2, IAzApplication2::InitializeClientContextFromToken2, InitializeClientContextFromToken2, InitializeClientContextFromToken2 method [Security], InitializeClientContextFromToken2 method [Security],IAzApplication2 interface, azroles/IAzApplication2::InitializeClientContextFromToken2, security.iazapplication2_initializeclientcontextfromtoken2
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IAzApplication2::InitializeClientContextFromToken2
 - azroles/IAzApplication2::InitializeClientContextFromToken2
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
 - IAzApplication2.InitializeClientContextFromToken2
---

# IAzApplication2::InitializeClientContextFromToken2


## -description

The <b>InitializeClientContextFromToken2</b> method retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a> object pointer from the specified client token.

## -parameters

### -param ulTokenHandleLowPart [in]

Low byte of a handle to a token that specifies the client. If the values of both this parameter and the <i>ulTokenHandleHighPart</i> parameter are zero, the impersonation token of the caller's thread is used. If the thread does not have an impersonation token, the process token is used. The token must have been opened for TOKEN_QUERY, TOKEN_IMPERSONATE, or TOKEN_DUPLICATE access.

### -param ulTokenHandleHighPart [in]

High byte of a handle to a token that specifies the client. If the values of both this parameter and the <i>ulTokenHandleHighPart</i> parameter are zero, the impersonation token of the caller's thread is used. If the thread does not have an impersonation token, the process token is used. The token must have been opened for TOKEN_QUERY, TOKEN_IMPERSONATE, or TOKEN_DUPLICATE access.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppClientContext [out]

A pointer to a pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.
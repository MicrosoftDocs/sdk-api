---
UID: NF:azroles.IAzApplication2.InitializeClientContextFromToken2
title: IAzApplication2::InitializeClientContextFromToken2
author: windows-sdk-content
description: Retrieves an IAzClientContext2 object pointer from the specified client token.
old-location: security\iazapplication2_initializeclientcontextfromtoken2.htm
old-project: SecAuthZ
ms.assetid: f77b5eb1-c121-4392-a317-7021059268ed
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IAzApplication2 interface [Security],InitializeClientContextFromToken2 method, IAzApplication2.InitializeClientContextFromToken2, IAzApplication2::InitializeClientContextFromToken2, InitializeClientContextFromToken2, InitializeClientContextFromToken2 method [Security], InitializeClientContextFromToken2 method [Security],IAzApplication2 interface, azroles/IAzApplication2::InitializeClientContextFromToken2, security.iazapplication2_initializeclientcontextfromtoken2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication2.InitializeClientContextFromToken2
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication2::InitializeClientContextFromToken2


## -description


The <b>InitializeClientContextFromToken2</b> method retrieves an <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> object pointer from the specified client token.


## -parameters




### -param ulTokenHandleLowPart [in]

Low byte of a handle to a token that specifies the client. If the values of both this parameter and the <i>ulTokenHandleHighPart</i> parameter are zero, the impersonation token of the caller's thread is used. If the thread does not have an impersonation token, the process token is used. The token must have been opened for TOKEN_QUERY, TOKEN_IMPERSONATE, or TOKEN_DUPLICATE access.


### -param ulTokenHandleHighPart [in]

High byte of a handle to a token that specifies the client. If the values of both this parameter and the <i>ulTokenHandleHighPart</i> parameter are zero, the impersonation token of the caller's thread is used. If the thread does not have an impersonation token, the process token is used. The token must have been opened for TOKEN_QUERY, TOKEN_IMPERSONATE, or TOKEN_DUPLICATE access.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppClientContext






#### - ppClientContext2 [out]

A pointer to a pointer to the returned <a href="https://msdn.microsoft.com/8e922370-18e3-481c-93f2-9a56d7898ba7">IAzClientContext2</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




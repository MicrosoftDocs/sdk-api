---
UID: NF:azroles.IAzApplication.InitializeClientContextFromToken
title: IAzApplication::InitializeClientContextFromToken method
author: windows-driver-content
description: Gets an IAzClientContext object pointer from the specified client token.
old-location: security\iazapplication_initializeclientcontextfromtoken.htm
old-project: SecAuthZ
ms.assetid: 0002804d-0e97-4648-8aa1-14eba09a90fa
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AzApplication object [Security], InitializeClientContextFromToken method, IAzApplication, IAzApplication interface [Security], InitializeClientContextFromToken method, IAzApplication::InitializeClientContextFromToken, InitializeClientContextFromToken method [Security], InitializeClientContextFromToken method [Security], AzApplication object, InitializeClientContextFromToken method [Security], IAzApplication interface, InitializeClientContextFromToken,IAzApplication.InitializeClientContextFromToken, azroles/IAzApplication::InitializeClientContextFromToken, security.iazapplication_initializeclientcontextfromtoken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	IAzApplication.InitializeClientContextFromToken
-	AzApplication.InitializeClientContextFromToken
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::InitializeClientContextFromToken method


## -description


The <b>InitializeClientContextFromToken</b> method gets an <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> object pointer from the specified client token.


## -parameters




### -param ullTokenHandle [in]

A handle to a Windows token that specifies the client. If this parameter is <b>NULL</b>, the impersonation token of the caller's thread is used. If the thread does not have an impersonation token, the process token is used. The token must have been opened for TOKEN_QUERY, TOKEN_IMPERSONATE, and TOKEN_DUPLICATE access.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppClientContext [out]

A pointer to a pointer to the returned <a href="https://msdn.microsoft.com/e24184d2-a77b-4a8b-b2f3-78f1e0b902f9">IAzClientContext</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




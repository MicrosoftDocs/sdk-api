---
UID: NF:authz.AuthzInitializeRemoteResourceManager
title: AuthzInitializeRemoteResourceManager function
author: windows-sdk-content
description: Allocates and initializes a remote resource manager. The caller can use the resulting handle to make RPC calls to a remote instance of the resource manager configured on a server.
old-location: security\authzinitializeremoteresourcemanager.htm
old-project: SecAuthZ
ms.assetid: C3B6C75B-13A5-49CC-BB01-DA1EEC292C20
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AuthzInitializeRemoteResourceManager, AuthzInitializeRemoteResourceManager function [Security], authz/AuthzInitializeRemoteResourceManager, security.authzinitializeremoteresourcemanager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: authz.h
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
req.typenames: AUTHZ_CONTEXT_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Authz.dll
api_name:
-	AuthzInitializeRemoteResourceManager
product: Windows
targetos: Windows
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
---

# AuthzInitializeRemoteResourceManager function


## -description


The <b>AuthzInitializeRemoteResourceManager</b> function allocates and initializes a remote resource manager. The caller can use the resulting handle to make AuthZ calls over RPC to a remote instance of the resource manager configured on a server.


## -parameters




### -param pRpcInitInfo [in]

Pointer to an <a href="https://msdn.microsoft.com/6859A0CB-F88E-42BF-A350-293D28E908DD">AUTHZ_RPC_INIT_INFO_CLIENT</a> structure containing the initial information needed to configure the connection.


### -param phAuthzResourceManager [out]

A handle to the resource manager. When you have finished using the handle, free it by calling the <a href="https://msdn.microsoft.com/8b716368-8d81-4c62-9086-0976b39bbcf8">AuthzFreeResourceManager</a> function.


## -returns




						If the function succeeds, the function returns <b>TRUE</b>. 

If the function fails, it returns <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




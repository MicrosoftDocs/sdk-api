---
UID: NF:authz.AuthzInitializeRemoteResourceManager
title: AuthzInitializeRemoteResourceManager function (authz.h)
description: Allocates and initializes a remote resource manager. The caller can use the resulting handle to make RPC calls to a remote instance of the resource manager configured on a server.
helpviewer_keywords: ["AuthzInitializeRemoteResourceManager","AuthzInitializeRemoteResourceManager function [Security]","authz/AuthzInitializeRemoteResourceManager","security.authzinitializeremoteresourcemanager"]
old-location: security\authzinitializeremoteresourcemanager.htm
tech.root: security
ms.assetid: C3B6C75B-13A5-49CC-BB01-DA1EEC292C20
ms.date: 12/05/2018
ms.keywords: AuthzInitializeRemoteResourceManager, AuthzInitializeRemoteResourceManager function [Security], authz/AuthzInitializeRemoteResourceManager, security.authzinitializeremoteresourcemanager
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuthzInitializeRemoteResourceManager
 - authz/AuthzInitializeRemoteResourceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzInitializeRemoteResourceManager
---

# AuthzInitializeRemoteResourceManager function


## -description

The <b>AuthzInitializeRemoteResourceManager</b> function allocates and initializes a remote resource manager. The caller can use the resulting handle to make AuthZ calls over RPC to a remote instance of the resource manager configured on a server.

## -parameters

### -param pRpcInitInfo [in]

Pointer to an <a href="/windows/desktop/api/authz/ns-authz-authz_rpc_init_info_client">AUTHZ_RPC_INIT_INFO_CLIENT</a> structure containing the initial information needed to configure the connection.

### -param phAuthzResourceManager [out]

A handle to the resource manager. When you have finished using the handle, free it by calling the <a href="/windows/desktop/api/authz/nf-authz-authzfreeresourcemanager">AuthzFreeResourceManager</a> function.

## -returns

If the function succeeds, the function returns <b>TRUE</b>. 

If the function fails, it returns <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
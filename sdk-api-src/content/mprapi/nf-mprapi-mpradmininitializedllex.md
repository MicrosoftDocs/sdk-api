---
UID: NF:mprapi.MprAdminInitializeDllEx
title: MprAdminInitializeDllEx function (mprapi.h)
description: When the Routing and Remote Access Service (RRAS) starts, it calls the MprAdminInitializeDll function that is exported by the administration DLL.
helpviewer_keywords: ["MprAdminInitializeDllEx","MprAdminInitializeDllEx callback","MprAdminInitializeDllEx callback function [RAS]","mprapi/MprAdminInitializeDllEx","rras.mpradmininitializedllex"]
old-location: rras\mpradmininitializedllex.htm
tech.root: RRAS
ms.assetid: c608c1b3-39de-4c0f-b834-27b9211dffb5
ms.date: 12/05/2018
ms.keywords: MprAdminInitializeDllEx, MprAdminInitializeDllEx callback, MprAdminInitializeDllEx callback function [RAS], mprapi/MprAdminInitializeDllEx, rras.mpradmininitializedllex
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminInitializeDllEx
 - mprapi/MprAdminInitializeDllEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mprapi.h
api_name:
 - MprAdminInitializeDllEx
---

# MprAdminInitializeDllEx function


## -description

When the Routing and Remote Access Service (RRAS) starts, it calls the 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininitializedll">MprAdminInitializeDll</a> function that is exported by the administration DLL. Use this function to perform any required initialization for the DLL and call the callback functions. This serves as a placeholder for the callback functions.

## -parameters

### -param pAdminCallbacks

A pointer to a <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_admin_dll_callbacks">MPRAPI_ADMIN_DLL_CALLBACKS</a> structure that contains the function pointers of the callbacks being registered.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function returns any value other than <b>NO_ERROR</b>, RRAS will fail to start.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininitializedll">MprAdminInitializeDll</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminterminatedll">MprAdminTerminateDll</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
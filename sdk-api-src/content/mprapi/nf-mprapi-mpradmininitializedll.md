---
UID: NF:mprapi.MprAdminInitializeDll
title: MprAdminInitializeDll function (mprapi.h)
description: When the Routing and Remote Access Service (RRAS) starts, it calls the MprAdminInitializeDll function that is exported by the administration DLL. Use this function to perform any required initialization for the DLL.
helpviewer_keywords: ["MprAdminInitializeDll","MprAdminInitializeDll callback","MprAdminInitializeDll callback function [RAS]","_mpr_mpradmininitializedll","mprapi/MprAdminInitializeDll","rras.mpradmininitializedll"]
old-location: rras\mpradmininitializedll.htm
tech.root: RRAS
ms.assetid: 0a53d84e-d9be-4d18-a619-7d92c17b76bb
ms.date: 12/05/2018
ms.keywords: MprAdminInitializeDll, MprAdminInitializeDll callback, MprAdminInitializeDll callback function [RAS], _mpr_mpradmininitializedll, mprapi/MprAdminInitializeDll, rras.mpradmininitializedll
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - MprAdminInitializeDll
 - mprapi/MprAdminInitializeDll
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
 - MprAdminInitializeDll
---

# MprAdminInitializeDll function


## -description

When the Routing and Remote Access Service (RRAS) starts, it calls the 
<b>MprAdminInitializeDll</b> function that is exported by the administration DLL. Use this function to perform any required initialization for the DLL.



## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function returns any value other than <b>NO_ERROR</b>, RRAS will fail to start.

## -remarks

RAS supports multiple Administration DLLs. RAS calls the multiple implementations of <b>MprAdminInitializeDll</b> in the order in which the DLLs are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>.

This function can return any of the error codes that are defined in the Winerror.h header file in the Platform Software Development Kit (SDK).

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminterminatedll">MprAdminTerminateDll</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>

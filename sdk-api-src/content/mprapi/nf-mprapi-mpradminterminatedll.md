---
UID: NF:mprapi.MprAdminTerminateDll
title: MprAdminTerminateDll function (mprapi.h)
description: When the RAS shuts down, it calls the MprAdminTerminateDll function exported by the administration DLL. Use this function to perform any required clean-up for the DLL.
old-location: rras\mpradminterminatedll.htm
tech.root: RRAS
ms.assetid: 7be485ce-fd45-4968-9e9d-2128d5a8967d
ms.date: 12/05/2018
ms.keywords: MprAdminTerminateDll, MprAdminTerminateDll callback, MprAdminTerminateDll callback function [RAS], _mpr_mpradminterminatedll, mprapi/MprAdminTerminateDll, rras.mpradminterminatedll
f1_keywords:
- mprapi/MprAdminTerminateDll
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Mprapi.h
api_name:
- MprAdminTerminateDll
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminTerminateDll function


## -description


When the RAS shuts down, it calls the 
<b>MprAdminTerminateDll</b> function exported by the administration DLL. Use this function to perform any required clean-up for the DLL.


## -parameters






## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.




## -remarks



RAS supports multiple Administration DLLs. RAS calls the multiple implementations of <a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininitializedll">MprAdminInitializeDll</a> in the order in which the DLLs are listed in the 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmininitializedll">MprAdminInitializeDll</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
 

 


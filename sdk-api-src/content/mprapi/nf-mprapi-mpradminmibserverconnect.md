---
UID: NF:mprapi.MprAdminMIBServerConnect
title: MprAdminMIBServerConnect function (mprapi.h)
description: The MprAdminMIBServerConnect function establishes a connection to the router being administered. This call should be made before any other calls to the server. The handle returned by this function is used in subsequent MIB calls.
helpviewer_keywords: ["MprAdminMIBServerConnect","MprAdminMIBServerConnect function [RAS]","_mpr_mpradminmibserverconnect","mprapi/MprAdminMIBServerConnect","rras.mpradminmibserverconnect"]
old-location: rras\mpradminmibserverconnect.htm
tech.root: RRAS
ms.assetid: 8d8cba34-e5d3-42ae-9724-361802f21410
ms.date: 12/05/2018
ms.keywords: MprAdminMIBServerConnect, MprAdminMIBServerConnect function [RAS], _mpr_mpradminmibserverconnect, mprapi/MprAdminMIBServerConnect, rras.mpradminmibserverconnect
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminMIBServerConnect
 - mprapi/MprAdminMIBServerConnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminMIBServerConnect
---

# MprAdminMIBServerConnect function


## -description

The 
<b>MprAdminMIBServerConnect</b> function establishes a connection to the router being administered. This call should be made before any other calls to the server. The handle returned by this function is used in subsequent MIB calls.

## -parameters

### -param lpwsServerName [in]

Pointer to a Unicode string that specifies the name of the remote server. If the caller specifies <b>NULL</b> for this parameter, the function returns a handle to the local server.

### -param phMibServer [out]

Pointer to a handle variable. This variable receives a handle to the server.

## -returns

If the function succeeds, the return value is NO_ERROR.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverdisconnect">MprAdminMIBServerDisconnect</a>



<a href="/windows/desktop/RRAS/mib-functions">Router Management MIB Functions</a>



<a href="/windows/desktop/RRAS/router-management-mib-reference">Router Management MIB Reference</a>
---
UID: NF:mprapi.MprAdminMIBServerDisconnect
title: MprAdminMIBServerDisconnect function (mprapi.h)
description: The MprAdminMIBServerDisconnect function disconnects the connection made by a previous call to MprAdminMIBServerConnect.
helpviewer_keywords: ["MprAdminMIBServerDisconnect","MprAdminMIBServerDisconnect function [RAS]","_mpr_mpradminmibserverdisconnect","mprapi/MprAdminMIBServerDisconnect","rras.mpradminmibserverdisconnect"]
old-location: rras\mpradminmibserverdisconnect.htm
tech.root: RRAS
ms.assetid: 63ea910a-b9d7-43a3-97ae-2f9c26b52059
ms.date: 12/05/2018
ms.keywords: MprAdminMIBServerDisconnect, MprAdminMIBServerDisconnect function [RAS], _mpr_mpradminmibserverdisconnect, mprapi/MprAdminMIBServerDisconnect, rras.mpradminmibserverdisconnect
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
 - MprAdminMIBServerDisconnect
 - mprapi/MprAdminMIBServerDisconnect
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
 - MprAdminMIBServerDisconnect
---

# MprAdminMIBServerDisconnect function


## -description

The 
<b>MprAdminMIBServerDisconnect</b> function disconnects the connection made by a previous call to 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>.

## -parameters

### -param hMibServer [in]

Handle to the router from which to disconnect. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>



<a href="/windows/desktop/RRAS/mib-functions">Router Management MIB Functions</a>



<a href="/windows/desktop/RRAS/router-management-mib-reference">Router Management MIB Reference</a>
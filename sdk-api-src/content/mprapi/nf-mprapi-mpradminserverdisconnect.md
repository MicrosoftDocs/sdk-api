---
UID: NF:mprapi.MprAdminServerDisconnect
title: MprAdminServerDisconnect function (mprapi.h)
description: The MprAdminServerDisconnect function disconnects the connection made by a previous call to MprAdminServerConnect.
old-location: rras\mpradminserverdisconnect.htm
tech.root: RRAS
ms.assetid: 905b5296-ae6b-40a6-ba49-837db96de152
ms.date: 12/05/2018
ms.keywords: MprAdminServerDisconnect, MprAdminServerDisconnect function [RAS], _mpr_mpradminserverdisconnect, mprapi/MprAdminServerDisconnect, rras.mpradminserverdisconnect
f1_keywords:
- mprapi/MprAdminServerDisconnect
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Mprapi.dll
api_name:
- MprAdminServerDisconnect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminServerDisconnect function


## -description


The 
<b>MprAdminServerDisconnect</b> function disconnects the connection made by a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.


## -parameters




### -param hMprServer [in]

Handle to the router from which to disconnect. Obtain this handle by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
 

 


---
UID: NF:mprapi.MprAdminConnectionHangupNotification2
title: MprAdminConnectionHangupNotification2 function (mprapi.h)
description: Remote Access Service calls the MprAdminConnectionHangupNotification2 function after the last link for the specified connection has been dismantled.helpviewer_keywords: ["MprAdminConnectionHangupNotification2","MprAdminConnectionHangupNotification2 callback","MprAdminConnectionHangupNotification2 callback function [RAS]","_mpr_mpradminconnectionhangupnotification2","mprapi/MprAdminConnectionHangupNotification2","rras.mpradminconnectionhangupnotification2"]
old-location: rras\mpradminconnectionhangupnotification2.htm
tech.root: RRAS
ms.assetid: 3231ae83-c7fc-46d4-a4d9-f7ccf1c4ed18
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionHangupNotification2, MprAdminConnectionHangupNotification2 callback, MprAdminConnectionHangupNotification2 callback function [RAS], _mpr_mpradminconnectionhangupnotification2, mprapi/MprAdminConnectionHangupNotification2, rras.mpradminconnectionhangupnotification2
f1_keywords:
- mprapi/MprAdminConnectionHangupNotification2
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
- MprAdminConnectionHangupNotification2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminConnectionHangupNotification2 function


## -description


Remote Access Service calls the 
<b>MprAdminConnectionHangupNotification2</b> function after the last link for the specified connection has been dismantled.


## -parameters




### -param pRasConnection0 [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a> structure that describes this connection.


### -param pRasConnection1 [in]

Pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a> structure that describes this connection.


### -param pRasConnection2 [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a> structure that describes this connection.


## -remarks



RAS supports multiple Administration DLLs. RAS calls the multiple implementations of the 
<b>MprAdminConnectionHangupNotification2</b> function in the order in which the DLLs are listed in the 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>.

<b>Windows 2000 Server and earlier:  </b>If 
<b>MprAdminAcceptNewConnection</b> does not accept the new connection, RAS does not call the 
<b>MprAdminConnectionHangupNotification2</b> function.

Do not call any of the 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminConnectionHangupNotification2</b>. Calls to these functions do not return when made from within a callout function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection">MprAdminAcceptNewConnection2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewlink">MprAdminAcceptNewLink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification3">MprAdminConnectionHangupNotification3</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
 

 


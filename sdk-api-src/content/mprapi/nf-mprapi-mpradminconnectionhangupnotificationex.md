---
UID: NF:mprapi.MprAdminConnectionHangupNotificationEx
title: MprAdminConnectionHangupNotificationEx function (mprapi.h)
description: Remote Access Service (RAS) calls the MprAdminConnectionHangupNotificationEx function after the last link for the specified connection has been dismantled.
helpviewer_keywords: ["MprAdminConnectionHangupNotificationEx","MprAdminConnectionHangupNotificationEx callback","MprAdminConnectionHangupNotificationEx callback function [RAS]","mprapi/MprAdminConnectionHangupNotificationEx","rras.mpradminconnectionhangupnotificationex"]
old-location: rras\mpradminconnectionhangupnotificationex.htm
tech.root: RRAS
ms.assetid: de251e1b-53ff-45c8-8e2e-65ac26b4a7f5
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionHangupNotificationEx, MprAdminConnectionHangupNotificationEx callback, MprAdminConnectionHangupNotificationEx callback function [RAS], mprapi/MprAdminConnectionHangupNotificationEx, rras.mpradminconnectionhangupnotificationex
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
 - MprAdminConnectionHangupNotificationEx
 - mprapi/MprAdminConnectionHangupNotificationEx
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
 - MprAdminConnectionHangupNotificationEx
---

# MprAdminConnectionHangupNotificationEx function


## -description

Remote Access Service (RAS) calls the 
<b>MprAdminConnectionHangupNotificationEx</b> function after the last link for the specified connection has been dismantled.

## -parameters

### -param pRasConn [in]

A pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure that describes this connection.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification2">MprAdminConnectionHangupNotification2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification3">MprAdminConnectionHangupNotification3</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
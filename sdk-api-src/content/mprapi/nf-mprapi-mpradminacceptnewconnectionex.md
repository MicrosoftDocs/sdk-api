---
UID: NF:mprapi.MprAdminAcceptNewConnectionEx
title: MprAdminAcceptNewConnectionEx function (mprapi.h)
description: Remote Access Service (RAS) calls the MprAdminAcceptNewConnectionEx function each time a new user dials in and successfully completes a RAS authentication. MprAdminAcceptNewConnectionEx determines whether the user is allowed to connect.
helpviewer_keywords: ["MprAdminAcceptNewConnectionEx","MprAdminAcceptNewConnectionEx callback","MprAdminAcceptNewConnectionEx callback function [RAS]","mprapi/MprAdminAcceptNewConnectionEx","rras.mpradminacceptnewconnectionex"]
old-location: rras\mpradminacceptnewconnectionex.htm
tech.root: RRAS
ms.assetid: 398dd922-dd83-402f-b7ad-ce9438f15ca9
ms.date: 12/05/2018
ms.keywords: MprAdminAcceptNewConnectionEx, MprAdminAcceptNewConnectionEx callback, MprAdminAcceptNewConnectionEx callback function [RAS], mprapi/MprAdminAcceptNewConnectionEx, rras.mpradminacceptnewconnectionex
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
 - MprAdminAcceptNewConnectionEx
 - mprapi/MprAdminAcceptNewConnectionEx
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
 - MprAdminAcceptNewConnectionEx
---

# MprAdminAcceptNewConnectionEx function


## -description

Remote Access Service (RAS) calls the 
<b>MprAdminAcceptNewConnectionEx</b> function each time a new user dials in and successfully completes a RAS authentication. <b>MprAdminAcceptNewConnectionEx</b> determines whether the user is allowed to connect.

## -parameters

### -param pRasConn [in]

A pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure that describes this connection.

## -returns

This callback function does not return a value.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection">MprAdminAcceptNewConnection</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection2">MprAdminAcceptNewConnection2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection3">MprAdminAcceptNewConnection3</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
---
UID: NF:mprapi.MprAdminSendUserMessage
title: MprAdminSendUserMessage function (mprapi.h)
description: The MprAdminSendUserMessage function sends a message to the user connected on the specified connection.
helpviewer_keywords: ["MprAdminSendUserMessage","MprAdminSendUserMessage function [RAS]","_mpr_mpradminsendusermessage","mprapi/MprAdminSendUserMessage","rras.mpradminsendusermessage"]
old-location: rras\mpradminsendusermessage.htm
tech.root: RRAS
ms.assetid: 3c0d8b6c-25c1-47c3-baef-d82e6d2fa52f
ms.date: 12/05/2018
ms.keywords: MprAdminSendUserMessage, MprAdminSendUserMessage function [RAS], _mpr_mpradminsendusermessage, mprapi/MprAdminSendUserMessage, rras.mpradminsendusermessage
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminSendUserMessage
 - mprapi/MprAdminSendUserMessage
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
 - MprAdminSendUserMessage
---

# MprAdminSendUserMessage function


## -description

The 
<b>MprAdminSendUserMessage</b> function sends a message to the user connected on the specified connection.

## -parameters

### -param hMprServer [in]

Handle to the RAS server on which the user is connected. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param hConnection [in]

Handle to the connection on which the user is connected. Use 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a> to obtain this handle.

### -param lpwszMessage [in]

Pointer to a Unicode string that specifies the message to the user.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Demand Dial Manager (DDM) is not running, possibly because the Dynamic Interface Manager (DIM) is configured to run only on a LAN.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERFACE_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>hConnection</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpwszMessage</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
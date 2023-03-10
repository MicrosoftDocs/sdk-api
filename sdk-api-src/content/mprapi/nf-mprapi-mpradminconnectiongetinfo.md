---
UID: NF:mprapi.MprAdminConnectionGetInfo
title: MprAdminConnectionGetInfo function (mprapi.h)
description: Retrieves data about a specific connection.
helpviewer_keywords: ["MprAdminConnectionGetInfo","MprAdminConnectionGetInfo function [RAS]","_mpr_mpradminconnectiongetinfo","mprapi/MprAdminConnectionGetInfo","rras.mpradminconnectiongetinfo"]
old-location: rras\mpradminconnectiongetinfo.htm
tech.root: RRAS
ms.assetid: 1fef5fbf-de3f-43c6-8b94-808f6ed209d8
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionGetInfo, MprAdminConnectionGetInfo function [RAS], _mpr_mpradminconnectiongetinfo, mprapi/MprAdminConnectionGetInfo, rras.mpradminconnectiongetinfo
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
 - MprAdminConnectionGetInfo
 - mprapi/MprAdminConnectionGetInfo
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
 - MprAdminConnectionGetInfo
---

# MprAdminConnectionGetInfo function


## -description

The 
<b>MprAdminConnectionGetInfo</b> function retrieves data about a specific connection.

## -parameters

### -param hRasServer [in]

A handle to the computer from which the connection information is retrieved. To obtain this handle, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, 2, and 3, as listed in the following table.

<b>Windows NT 4.0:  </b>This parameter must be zero.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>Windows 2000 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>Windows 2000 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>
</td>
</tr>
<tr>
<td>3</td>
<td>Windows Server 2008 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>
</td>
</tr>
</table>

### -param hRasConnection [in]

A handle to the connection to retrieve data about. To obtain this handle, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>.

### -param lplpbBuffer [out]

On successful completion, a pointer to an array of structures that describe the connection. These structures are of type <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>, <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>, <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>, or <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>, depending on the value of the <i>dwLevel</i> parameter. 

To free this memory, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the error codes listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The handle to the RAS server or the handle to the RAS connection is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value passed for <i>dwLevel</i> is not zero, one, two, or three. Levels one and two are supported only on Windows 2000 or later. Level three is supported only on Windows Server 2008 or later.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INTERFACE_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
 The <i>hConnection</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The <i>hRasServer</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error from MprError.h, RasError.h, or WinError.h.

</td>
</tr>
</table>

## -remarks

This function is available on Windows NT 4.0 if the RRAS redistributable is installed. However, the version of Mprapi.dll included in the RRAS redistributable exports the function as <b>RasAdminConnectionGetInfo</b> rather than 
<b>MprAdminConnectionGetInfo</b>. Therefore, when using the RRAS redistributable, use 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access this function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
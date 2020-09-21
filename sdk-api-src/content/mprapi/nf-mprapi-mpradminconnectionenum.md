---
UID: NF:mprapi.MprAdminConnectionEnum
title: MprAdminConnectionEnum function (mprapi.h)
description: The MprAdminConnectionEnum function enumerates all active connections.
helpviewer_keywords: ["MprAdminConnectionEnum","MprAdminConnectionEnum function [RAS]","_mpr_mpradminconnectionenum","mprapi/MprAdminConnectionEnum","rras.mpradminconnectionenum"]
old-location: rras\mpradminconnectionenum.htm
tech.root: RRAS
ms.assetid: 27be536e-0437-4e30-aef7-ed92f50baeaa
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionEnum, MprAdminConnectionEnum function [RAS], _mpr_mpradminconnectionenum, mprapi/MprAdminConnectionEnum, rras.mpradminconnectionenum
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
 - MprAdminConnectionEnum
 - mprapi/MprAdminConnectionEnum
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
 - MprAdminConnectionEnum
---

# MprAdminConnectionEnum function


## -description

The 
<b>MprAdminConnectionEnum</b> function enumerates all active connections.

## -parameters

### -param hRasServer [in]

Handle to the RAS server on which connections are enumerated. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

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

### -param lplpbBuffer [out]

On successful completion, a pointer to an array of structures that describe the connection. These structures are of type <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>, <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>, <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>, or <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>, depending on the value of the <i>dwLevel</i> parameter. 

To free this memory, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

### -param dwPrefMaxLen [in]

Specifies the preferred maximum length of returned data in 8-bit bytes. If <i>dwPrefMaxLen</i> is -1, the buffer returned is large enough to hold all available information.

### -param lpdwEntriesRead [out]

Pointer to a <b>DWORD</b> variable. This variable receives the total number of connections enumerated from the current resume position.

### -param lpdwTotalEntries [out]

Pointer to a <b>DWORD</b> variable. This variable receives the total number of connections that could have been enumerated from the current resume position.

### -param lpdwResumeHandle [in]

Pointer to a <b>DWORD</b> variable. This variable specifies a resume handle used to continue the enumeration. The <i>lpdwResumeHandle</i> parameter is zero on the first call, and left unchanged on subsequent calls. If the return code is ERROR_MORE_DATA, another call may be made using this handle to retrieve more data. If the handle is <b>NULL</b> upon return, the enumeration is complete. This handle is invalid for other types of error returns.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following parameters is <b>NULL</b> or does not point to valid memory: <i>lplpBuffer</i>, <i>lpdwEntriesRead</i>, or <i>lpdwTotalEntries</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Not all of the data was returned with this call. To obtain additional data, call the function again using the resume handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The handle passed in the <i>hRasServer</i> parameter is <b>NULL</b> or invalid.

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

This function is available on Windows NT 4.0 if the RRAS redistributable is installed. However, the version of Mprapi.dll that ships with the RRAS redistributable exports the function as <b>RasAdminConnectionEnum</b> rather than 
<b>MprAdminConnectionEnum</b>. Therefore, when using the RRAS redistributable, use 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access this function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
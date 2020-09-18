---
UID: NF:mprapi.MprAdminPortEnum
title: MprAdminPortEnum function (mprapi.h)
description: Enumerates all active ports in a specific connection, or all ports available for use or currently used by RAS.
helpviewer_keywords: ["MprAdminPortEnum","MprAdminPortEnum function [RAS]","_mpr_mpradminportenum","mprapi/MprAdminPortEnum","rras.mpradminportenum"]
old-location: rras\mpradminportenum.htm
tech.root: RRAS
ms.assetid: b6caa1f0-f4c7-48a9-b1e8-b484e7d7a3a3
ms.date: 12/05/2018
ms.keywords: MprAdminPortEnum, MprAdminPortEnum function [RAS], _mpr_mpradminportenum, mprapi/MprAdminPortEnum, rras.mpradminportenum
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
 - MprAdminPortEnum
 - mprapi/MprAdminPortEnum
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
 - MprAdminPortEnum
---

# MprAdminPortEnum function


## -description

The 
<b>MprAdminPortEnum</b> function enumerates all active ports in a specific connection, or all ports available for use or currently used by RAS.

## -parameters

### -param hRasServer [in]

A handle to the RAS server whose ports are to be enumerated. To obtain this handle, call <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Must be zero.

### -param hRasConnection [in]

A handle to a connection for which the active ports are enumerated. If this parameter is <b>INVALID_HANDLE_VALUE</b>, all the ports in use or available for use by RRAS are enumerated. To obtain this handle, call 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>.

### -param lplpbBuffer [out]

On successful completion, a pointer to an array of <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a> structures that describes the port. Free this memory by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

### -param dwPrefMaxLen [in]

A value that specifies the preferred maximum length of returned data, in 8-bit bytes. If this parameter is -1, the buffer that is returned is large enough to hold all available data.

### -param lpdwEntriesRead [out]

A pointer to a <b>DWORD</b> variable. This variable receives the total number of ports that are enumerated from the current resume position.

### -param lpdwTotalEntries [out]

A pointer to a <b>DWORD</b> variable. This variable receives the total number of ports that could have been enumerated from the current resume position.

### -param lpdwResumeHandle [in]

A pointer to a <b>DWORD</b> variable. On successful execution, this parameter specifies a handle that can be used to resume the enumeration. This parameter should be zero on the first call and left unchanged on subsequent calls. If the return code is <b>ERROR_MORE_DATA</b>, the call can be reissued with the handle to retrieve more data. If the handle is <b>NULL</b> on return, the enumeration cannot be continued. This handle is invalid for other types of error returns.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the error codes listed in the following table.

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
The calling application does not have sufficient privileges.

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
Not all of the data was returned with this call. To obtain additional data, call the function again using the handle that was returned in the <i>IpdwResumeHandle</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> parameter is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hConnection</i> parameter is <b>NULL</b>.

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

If the RRAS redistributable is installed, this function is available on Windows NT 4.0. However, the version of Mprapi.dll that is provided with the RRAS redistributable exports the function as 
<b>RasAdminPortEnum</b> rather than 
<b>MprAdminPortEnum</b>. Therefore, when using the RRAS redistributable, use 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access this function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
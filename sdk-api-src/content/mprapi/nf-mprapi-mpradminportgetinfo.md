---
UID: NF:mprapi.MprAdminPortGetInfo
title: MprAdminPortGetInfo function (mprapi.h)
description: The MprAdminPortGetInfo function gets information for a specific port.
helpviewer_keywords: ["MprAdminPortGetInfo","MprAdminPortGetInfo function [RAS]","_mpr_mpradminportgetinfo","mprapi/MprAdminPortGetInfo","rras.mpradminportgetinfo"]
old-location: rras\mpradminportgetinfo.htm
tech.root: RRAS
ms.assetid: b990b2bf-6c08-4cfd-8b17-1b3fe39277d7
ms.date: 12/05/2018
ms.keywords: MprAdminPortGetInfo, MprAdminPortGetInfo function [RAS], _mpr_mpradminportgetinfo, mprapi/MprAdminPortGetInfo, rras.mpradminportgetinfo
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
 - MprAdminPortGetInfo
 - mprapi/MprAdminPortGetInfo
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
 - MprAdminPortGetInfo
---

# MprAdminPortGetInfo function


## -description

The 
<b>MprAdminPortGetInfo</b> function gets information for a specific port.

## -parameters

### -param hRasServer [in]

Handle to the RAS server computer on which to collect port information. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0 and 1 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a>
</td>
</tr>
</table>

### -param hPort [in]

Handle to the port for which to collect information. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminportenum">MprAdminPortEnum</a>.

### -param lplpbBuffer [out]

On successful completion, a pointer to a structure that describes the port. These structures are of type <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a> or <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a> depending on the value of the <i>dwLevel</i> parameter. Free this memory by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

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
<dt><b>ERROR_INVALID_PORT_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPort</i> parameter is invalid.

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
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error from MprError.h, RasError.h, or WinError.h.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

This function is available on Windows NT 4.0 if the RRAS redistributable is installed. However, the version of Mprapi.dll that ships with the RRAS redistributable exports the function as 
<b>RasAdminPortGetInfo</b> rather than 
<b>MprAdminPortGetInfo</b>. Therefore, when using the RRAS redistributable, use 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access this function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminportenum">MprAdminPortEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
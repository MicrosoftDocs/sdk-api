---
UID: NF:mprapi.MprAdminConnectionEnumEx
title: MprAdminConnectionEnumEx function (mprapi.h)
description: The MprAdminConnectionEnumEx function enumerates the active connections for a specified RRAS server.
helpviewer_keywords: ["MprAdminConnectionEnumEx","MprAdminConnectionEnumEx function [RAS]","mprapi/MprAdminConnectionEnumEx","rras.mpradminconnectionenumex"]
old-location: rras\mpradminconnectionenumex.htm
tech.root: RRAS
ms.assetid: 12507432-bf18-444d-9bcc-4ebc1418c083
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionEnumEx, MprAdminConnectionEnumEx function [RAS], mprapi/MprAdminConnectionEnumEx, rras.mpradminconnectionenumex
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminConnectionEnumEx
 - mprapi/MprAdminConnectionEnumEx
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
 - MprAdminConnectionEnumEx
---

# MprAdminConnectionEnumEx function


## -description

The 
<b>MprAdminConnectionEnumEx</b> function enumerates the active connections for a specified RRAS server.

## -parameters

### -param hRasServer [in]

A handle to the RAS server on which connections are enumerated. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param pObjectHeader [in]

A pointer to an <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_object_header">MPRAPI_OBJECT_HEADER</a>   structure that specifies the structure version received by <i>ppRasConn</i>.

### -param dwPreferedMaxLen [in]

A value that specifies the preferred maximum length of returned data in 8-bit bytes. If <i>dwPrefMaxLen</i> is -1, the buffer returned is large enough to hold all available information.

### -param lpdwEntriesRead [out]

A pointer to a <b>DWORD</b> that receives the total number of connections enumerated from the current resume position.

### -param lpdwTotalEntries [out]

A pointer to a <b>DWORD</b> that receives the total number of connections that could have been enumerated from the current resume position.

### -param ppRasConn [out]

A pointer, on output, to an array of <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structures that contain the active connection information for the RRAS server in  <i>hRasServer</i>. The number of array elements is determined by the value pointed to by <i>lpdwEntriesRead</i>.

### -param lpdwResumeHandle [in]

A pointer to a <b>DWORD</b> variable that specifies a resume handle used to continue the enumeration. The <i>lpdwResumeHandle</i> parameter is <b>NULL</b> on the first call, and left unchanged on subsequent calls. If the return code is <b>ERROR_MORE_DATA</b>, another call may be made using this handle to retrieve more data. If the handle is <b>NULL</b> upon return, the enumeration is complete. This handle is invalid for other types of error returns.

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
The Demand Dial Manager (DDM) is not running.

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
<dt><b>ERROR_PROC_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified procedure could not be found.

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

The caller should free the memory pointed to by <i>ppRasConn</i> by calling the function <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionenum">MprAdminConnectionEnum</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>
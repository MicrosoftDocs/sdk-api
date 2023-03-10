---
UID: NF:mprapi.MprConfigTransportEnum
title: MprConfigTransportEnum function (mprapi.h)
description: The MprConfigTransportEnum function enumerates the transports configured on the router.
helpviewer_keywords: ["MprConfigTransportEnum","MprConfigTransportEnum function [RAS]","_mpr_mprconfigtransportenum","mprapi/MprConfigTransportEnum","rras.mprconfigtransportenum"]
old-location: rras\mprconfigtransportenum.htm
tech.root: RRAS
ms.assetid: 2abe30f4-564b-499f-a6d3-13da305a783c
ms.date: 12/05/2018
ms.keywords: MprConfigTransportEnum, MprConfigTransportEnum function [RAS], _mpr_mprconfigtransportenum, mprapi/MprConfigTransportEnum, rras.mprconfigtransportenum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprConfigTransportEnum
 - mprapi/MprConfigTransportEnum
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
 - MprConfigTransportEnum
---

# MprConfigTransportEnum function


## -description

The 
<b>MprConfigTransportEnum</b> function enumerates the transports configured on the router.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration for the transports. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param dwLevel [in]

A <b>DWORD</b> value that describes the format in which the information is returned in the <i>lplpBuffer</i> parameter. Must be zero.

### -param lplpBuffer [in, out]

On input, a non-<b>NULL</b> pointer. 




On successful completion, a pointer to an array of 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_transport_0">MPR_TRANSPORT_0</a> structures. Free this memory buffer by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>.

### -param dwPrefMaxLen [in]

Specifies the preferred maximum length of returned data in 8-bit bytes. If this parameter is -1, the buffer returned will be large enough to hold all available information.

### -param lpdwEntriesRead [out]

Pointer to a <b>DWORD</b> variable. This variable receives the total number of entries that were enumerated from the current resume position.

### -param lpdwTotalEntries [out]

Pointer to a <b>DWORD</b> variable. This variable receives the total number of entries that could have been enumerated from the current resume position.

### -param lpdwResumeHandle [in, out, optional]

Pointer to a <b>DWORD</b> variable. 




On input, the handle should be zero on the first call and left unchanged on subsequent calls.

On output, this variable contains a resume handle used to continue the enumeration. If the handle is <b>NULL</b>, the enumeration is complete.

If an error occurs in the enumeration, this handle is invalid.

This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return a resume handle.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b>.</li>
<li><i>dwLevel</i> is not zero.</li>
<li><i>lplpBuffer</i> is <b>NULL</b>.</li>
<li><i>dwPrefMaxLen</i> is smaller than the size of a single 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_transport_0">MPR_TRANSPORT_0</a> structure.</li>
<li><i>lpdwEntriesRead</i> is <b>NULL</b>.</li>
<li><i>lpdwTotalEntries</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more entries available from the current resume position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
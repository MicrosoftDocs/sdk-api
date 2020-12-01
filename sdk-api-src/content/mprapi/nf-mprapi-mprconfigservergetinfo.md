---
UID: NF:mprapi.MprConfigServerGetInfo
title: MprConfigServerGetInfo function (mprapi.h)
description: The MprConfigServerGetInfo function retrieves server-level configuration information for the specified router.
helpviewer_keywords: ["MprConfigServerGetInfo","MprConfigServerGetInfo function [RAS]","_mpr_mprconfigservergetinfo","mprapi/MprConfigServerGetInfo","rras.mprconfigservergetinfo"]
old-location: rras\mprconfigservergetinfo.htm
tech.root: RRAS
ms.assetid: 6d3cd97a-96ef-4ecd-b2fd-2743ba79aa5b
ms.date: 12/05/2018
ms.keywords: MprConfigServerGetInfo, MprConfigServerGetInfo function [RAS], _mpr_mprconfigservergetinfo, mprapi/MprConfigServerGetInfo, rras.mprconfigservergetinfo
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
 - MprConfigServerGetInfo
 - mprapi/MprConfigServerGetInfo
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
 - MprConfigServerGetInfo
---

# MprConfigServerGetInfo function


## -description

The 
<b>MprConfigServerGetInfo</b> function retrieves server-level configuration information for the specified router.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, and 2 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>Windows 2000 Server or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>Windows Server 2003 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>Windows Server 2008 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a>
</td>
</tr>
</table>

### -param lplpbBuffer [out]

On successful completion, a pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>, 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>,  
or   <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					Free the memory for this buffer using 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: 




<ul>
<li>The <i>hMprConfig</i> parameter is <b>NULL</b>.</li>
<li>The <i>dwLevel</i> parameter is not zero.</li>
<li>The <i>lplpBuffer</i> parameter is <b>NULL</b>.</li>
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



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigbufferfree">MprConfigBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
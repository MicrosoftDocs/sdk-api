---
UID: NF:mprapi.MprConfigFilterGetInfo
title: MprConfigFilterGetInfo function (mprapi.h)
description: Returns static filtering information for a specified transport protocol type.
helpviewer_keywords: ["MprConfigFilterGetInfo","MprConfigFilterGetInfo function [RAS]","mprapi/MprConfigFilterGetInfo","rras.mprconfigfiltergetinfo"]
old-location: rras\mprconfigfiltergetinfo.htm
tech.root: RRAS
ms.assetid: d3c35418-57f4-4000-93c2-c04b5b0140ff
ms.date: 12/05/2018
ms.keywords: MprConfigFilterGetInfo, MprConfigFilterGetInfo function [RAS], mprapi/MprConfigFilterGetInfo, rras.mprconfigfiltergetinfo
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MprConfigFilterGetInfo
 - mprapi/MprConfigFilterGetInfo
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
 - MprConfigFilterGetInfo
---

# MprConfigFilterGetInfo function


## -description

The <b>MprConfigFilterGetInfo</b> function returns static filtering information for a specified  transport protocol type.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param dwLevel [in]

A <b>DWORD</b> value that describes the format in which the information is returned in the <i>lpBuffer</i> parameter. Must be zero.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport protocol type of the static filtering information in the <i>lpBuffer</i> parameter. Acceptable values for <i>dwTransportId</i> are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Transport (Protocol Family)</th>
</tr>
<tr>
<td>PID_ATALK</td>
<td>AppleTalk</td>
</tr>
<tr>
<td>PID_IP</td>
<td>Internet Protocol version 4</td>
</tr>
<tr>
<td>PID_IPX</td>
<td>Internet Packet Exchange</td>
</tr>
<tr>
<td>PID_NBF</td>
<td>NetBIOS Frames Protocol</td>
</tr>
<tr>
<td>PID_IPV6</td>
<td>Windows Server 2008 or later: Internet Protocol version 6</td>
</tr>
</table>

### -param lpBuffer [in_out]

On successful completion, writes a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_filter_0">MPR_FILTER_0</a> structure with the filter driver configuration information to the provided buffer. <i>lpBuffer</i> must be at least <i>sizeof(<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_filter_0">MPR_FILTER_0</a>)</i> bytes long.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

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
<i>hMprConfig</i> or <i>lpBuffer</i> is <b>NULL</b>, or <i>dwLevel</i> is not set to 0.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_filter_0">MPR_FILTER_0</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigfiltersetinfo">MprConfigFilterSetInfo</a>

---
UID: NF:mprapi.MprConfigTransportCreate
title: MprConfigTransportCreate function (mprapi.h)
description: The MprConfigTransportCreate function adds the specified transport to the list of transport protocols present in the specified router configuration.
helpviewer_keywords: ["MprConfigTransportCreate","MprConfigTransportCreate function [RAS]","_mpr_mprconfigtransportcreate","mprapi/MprConfigTransportCreate","rras.mprconfigtransportcreate"]
old-location: rras\mprconfigtransportcreate.htm
tech.root: RRAS
ms.assetid: a4cc4519-ce76-4619-b6dc-a5dfa18134e6
ms.date: 12/05/2018
ms.keywords: MprConfigTransportCreate, MprConfigTransportCreate function [RAS], _mpr_mprconfigtransportcreate, mprapi/MprConfigTransportCreate, rras.mprconfigtransportcreate
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
 - MprConfigTransportCreate
 - mprapi/MprConfigTransportCreate
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
 - MprConfigTransportCreate
---

# MprConfigTransportCreate function


## -description

The 
<b>MprConfigTransportCreate</b> function adds the specified transport to the list of transport protocols present in the specified router configuration.

## -parameters

### -param hMprConfig [in]

Handle to the router configuration to which to add the transport. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport to add to the configuration. This parameter also identifies the router manager for the transport. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

### -param lpwsTransportName [in, optional]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the transport being added. If this parameter is not specified, the <i>dwTransportId</i> parameter is converted into a string and used as the transport name.

### -param pGlobalInfo [in]

Pointer to an information header that specifies global information for the transport. The router manager for the transport interprets this information. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers.

### -param dwGlobalInfoSize [in]

Specifies the size, in bytes, of the data pointed to by the <i>pGlobalInfo</i> parameter.

### -param pClientInterfaceInfo [in, optional]

Pointer to an information header that specifies default interface information for client routers. This information is used to configure dynamic interfaces for client routers for this transport. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. 




This parameter is optional; the calling application can specify <b>NULL</b> for this parameter.

### -param dwClientInterfaceInfoSize [in, optional]

Specifies the size, in bytes, of the data pointed to by the <i>pClientInterfaceInfo</i> parameter. If the calling application specifies <b>NULL</b> for <i>pClientInterfaceInfo</i>, the calling application should specify zero for this parameter.

### -param lpwsDLLPath [in, optional]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the router manager DLL for the specified transport. If this name is specified, the function sets the DLL path for this transport to this name. 




This parameter is optional; the calling application can specify <b>NULL</b> for this parameter.

### -param phRouterTransport [out]

A pointer to a  
<b>HANDLE</b> variable that receives the transport configuration handle type indicated in the <i>dwTransportId</i> parameter.

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
The <i>hMprConfig</i> parameter is <b>NULL</b>, or the <i>phRouterTransport</i> parameter is <b>NULL</b>, or both are <b>NULL</b>.

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

## -remarks

If the specified transport already exists, 
<b>MprConfigTransportCreate</b> does the equivalent of an 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigtransportsetinfo">MprConfigTransportSetInfo</a> call using the supplied parameter values.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserverconnect">MprConfigServerConnect</a>



<a href="/windows/desktop/RRAS/router-configuration-functions">Router Configuration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
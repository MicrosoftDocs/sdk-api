---
UID: NF:mprapi.MprAdminMIBEntryGet
title: MprAdminMIBEntryGet function (mprapi.h)
description: The MprAdminMIBEntryGet function retrieves the value of one of the variables exported by a routing protocol or router manager.
helpviewer_keywords: ["MprAdminMIBEntryGet","MprAdminMIBEntryGet function [RAS]","_mpr_mpradminmibentryget","mprapi/MprAdminMIBEntryGet","rras.mpradminmibentryget"]
old-location: rras\mpradminmibentryget.htm
tech.root: RRAS
ms.assetid: 98e88364-4757-4b43-8316-6d4d9b3c2f29
ms.date: 12/05/2018
ms.keywords: MprAdminMIBEntryGet, MprAdminMIBEntryGet function [RAS], _mpr_mpradminmibentryget, mprapi/MprAdminMIBEntryGet, rras.mpradminmibentryget
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
 - MprAdminMIBEntryGet
 - mprapi/MprAdminMIBEntryGet
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
 - MprAdminMIBEntryGet
---

# MprAdminMIBEntryGet function


## -description

The 
<b>MprAdminMIBEntryGet</b> function retrieves the value of one of the variables exported by a routing protocol or router manager.

## -parameters

### -param hMibServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>.

### -param dwProtocolId [in]

Specifies the 
<a href="/windows/desktop/RRAS/transport-identifiers">router manager</a> that exported the variable.

### -param dwRoutingPid [in]

Specifies the 
<a href="/windows/desktop/RRAS/protocol-identifiers">routing protocol</a> that exported the variable.

### -param lpInEntry [in]

Pointer to an opaque data 
<a href="/previous-versions/windows/desktop/mib/mib-structures">structure</a>. The data structure's format is determined by the module servicing the call. The data structure should contain information that specifies the variable being queried.

### -param dwInEntrySize [in]

Specifies the size, in bytes, of the data structure pointed to by <i>lpInEntry</i>.

### -param lplpOutEntry [out]

Pointer to a pointer variable. On successful return, this pointer variable points to an opaque data 
<a href="/previous-versions/windows/desktop/mib/mib-structures">structure</a>. The data structure's format is determined by the module servicing the call. The data structure receives the value of the variable that was queried. Free this memory by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibbufferfree">MprAdminMIBBufferFree</a>.

### -param lpOutEntrySize [out]

Pointer to a <b>DWORD</b> variable that, on successful return, receives the size in bytes of the data structure returned through the <i>lplpOutEntry</i> parameter.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
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
<dt><b>ERROR_CANNOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwRoutingPid</i> variable does not match any installed routing protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any installed router manager.

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
</table>

## -remarks

Do not pass in <b>NULL</b> for the <i>lpInEntry</i> parameter because the resulting behavior is undefined.

## -see-also

<a href="/previous-versions/windows/desktop/mib/mib-structures">MIB Structures</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibbufferfree">MprAdminMIBBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrygetfirst">MprAdminMIBEntryGetFirst</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrygetnext">MprAdminMIBEntryGetNext</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentryset">MprAdminMIBEntrySet</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>



<a href="/windows/desktop/RRAS/obtaining-the-mib-ii-interfaces-table">Obtaining the MIB II Interfaces Table</a>



<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a>



<a href="/windows/desktop/RRAS/mib-functions">Router Management MIB Functions</a>



<a href="/windows/desktop/RRAS/router-management-mib-reference">Router Management MIB Reference</a>



<a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>
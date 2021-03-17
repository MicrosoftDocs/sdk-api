---
UID: NF:mprapi.MprAdminMIBEntryCreate
title: MprAdminMIBEntryCreate function (mprapi.h)
description: The MprAdminMIBEntryCreate function creates an entry for one of the variables exported by a routing protocol or router manager.
helpviewer_keywords: ["MprAdminMIBEntryCreate","MprAdminMIBEntryCreate function [RAS]","_mpr_mpradminmibentrycreate","mprapi/MprAdminMIBEntryCreate","rras.mpradminmibentrycreate"]
old-location: rras\mpradminmibentrycreate.htm
tech.root: RRAS
ms.assetid: b634ed78-ca01-4128-aeeb-fd8585e64f75
ms.date: 12/05/2018
ms.keywords: MprAdminMIBEntryCreate, MprAdminMIBEntryCreate function [RAS], _mpr_mpradminmibentrycreate, mprapi/MprAdminMIBEntryCreate, rras.mpradminmibentrycreate
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
 - MprAdminMIBEntryCreate
 - mprapi/MprAdminMIBEntryCreate
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
 - MprAdminMIBEntryCreate
---

# MprAdminMIBEntryCreate function


## -description

The 
<b>MprAdminMIBEntryCreate</b> function creates an entry for one of the variables exported by a routing protocol or router manager.

## -parameters

### -param hMibServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>.

### -param dwPid [out]

Receives the router manager that exported the variable.

### -param dwRoutingPid [in]

Specifies the routing protocol that exported the variable.

### -param lpEntry [in]

Pointer to an opaque data 
<a href="/previous-versions/windows/desktop/mib/mib-structures">structure</a>. The data structure's format is determined by the router manager or router manager client servicing the call. The data structure should contain information that specifies the variable being created and the value to assign to the variable.

### -param dwEntrySize [in]

Specifies the size, in bytes, of the data pointed to by the <i>lpEntry</i> parameter.

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
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwRoutingPid</i> variable does not match any installed routing protocol.

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
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any installed router manager.

</td>
</tr>
</table>

## -remarks

Do not pass in <b>NULL</b> for the <i>lpEntry</i> parameter because the resulting behavior is undefined.

## -see-also

<a href="/previous-versions/windows/desktop/mib/mib-structures">MIB Structures</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrydelete">MprAdminMIBEntryDelete</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>



<a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a>



<a href="/windows/desktop/RRAS/mib-functions">Router Management MIB Functions</a>



<a href="/windows/desktop/RRAS/router-management-mib-reference">Router Management MIB Reference</a>



<a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>
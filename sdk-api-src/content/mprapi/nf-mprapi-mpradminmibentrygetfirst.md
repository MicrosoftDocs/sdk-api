---
UID: NF:mprapi.MprAdminMIBEntryGetFirst
title: MprAdminMIBEntryGetFirst function (mprapi.h)
description: The MprAdminMIBEntryGetFirst function retrieves the first variable of some set of variables exported by a protocol or router manager. The module that services the call defines first.helpviewer_keywords: ["MprAdminMIBEntryGetFirst","MprAdminMIBEntryGetFirst function [RAS]","_mpr_mpradminmibentrygetfirst","mprapi/MprAdminMIBEntryGetFirst","rras.mpradminmibentrygetfirst"]
old-location: rras\mpradminmibentrygetfirst.htm
tech.root: RRAS
ms.assetid: e3c3ac47-d47c-4fd4-a064-b737bc40f190
ms.date: 12/05/2018
ms.keywords: MprAdminMIBEntryGetFirst, MprAdminMIBEntryGetFirst function [RAS], _mpr_mpradminmibentrygetfirst, mprapi/MprAdminMIBEntryGetFirst, rras.mpradminmibentrygetfirst
f1_keywords:
- mprapi/MprAdminMIBEntryGetFirst
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Mprapi.dll
api_name:
- MprAdminMIBEntryGetFirst
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminMIBEntryGetFirst function


## -description


The 
<b>MprAdminMIBEntryGetFirst</b> function retrieves the first variable of some set of variables exported by a protocol or router manager. The module that services the call defines <i>first</i>.


## -parameters




### -param hMibServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>.


### -param dwProtocolId [in]

Specifies the 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/transport-identifiers">router manager</a> that exported the variable.


### -param dwRoutingPid [in]

Specifies the 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/protocol-identifiers">routing protocol</a> that exported the variable.


### -param lpInEntry [in]

Pointer to an opaque data 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mib/mib-structures">structure</a>. The data structure's format is determined by the module servicing the call. The data structure should contain information that specifies the variable being queried.


### -param dwInEntrySize [in]

Specifies the size, in bytes, of the data pointed to by <i>lpInEntry</i>.


### -param lplpOutEntry [out]

Pointer to a pointer variable. On successful return, this pointer variable points to an opaque data 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mib/mib-structures">structure</a>. The data structure's format is determined by the module servicing the call. The data structure receives the value of the first variable from the set of variables exported. Free this memory by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibbufferfree">MprAdminMIBBufferFree</a>.


### -param lpOutEntrySize [out]

Pointer to a <b>DWORD</b> variable. On successful return, this variable receives the size, in bytes, of the data structure that was returned through the <i>lplpOutEntry</i> parameter.


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
The <i>dwTransportId</i> value does not match any installed transport/router manager.

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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mib/mib-structures">MIB Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibbufferfree">MprAdminMIBBufferFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentryget">MprAdminMIBEntryGet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibentrygetnext">MprAdminMIBEntryGetNext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/mib-functions">Router Management MIB Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-mib-reference">Router Management MIB Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>
 

 


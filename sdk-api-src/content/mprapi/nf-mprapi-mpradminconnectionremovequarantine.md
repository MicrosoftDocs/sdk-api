---
UID: NF:mprapi.MprAdminConnectionRemoveQuarantine
title: MprAdminConnectionRemoveQuarantine function (mprapi.h)
author: windows-sdk-content
description: The MprAdminConnectionRemoveQuarantine function removes quarantine filters on a dialed-in RAS client if the filters were applied as a result of Internet Authentication Service (IAS) policies.
old-location: rras\mpradminconnectionremovequarantine.htm
tech.root: RRAS
ms.assetid: 9d8c33b4-4227-4538-bc0e-f663d1d560f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionRemoveQuarantine, MprAdminConnectionRemoveQuarantine function [RAS], _mpr_mpradminconnectionremovequarantine, mprapi/MprAdminConnectionRemoveQuarantine, rras.mpradminconnectionremovequarantine
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - MprAdminConnectionRemoveQuarantine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminConnectionRemoveQuarantine function


## -description


The 
<b>MprAdminConnectionRemoveQuarantine</b> function removes quarantine filters on a dialed-in RAS client if the filters were applied as a result of Internet Authentication Service (IAS) policies.


## -parameters




### -param hRasServer [in]

Handle to the RAS server that services the connection. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>.


### -param hRasConnection [in]

Handle to connection for the RAS client for which to remove the quarantine filters. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>. 




Alternatively, this parameter specifies the IP address of the RAS client for which to remove the quarantine filter. The IP address should be specified as a <b>DWORD</b> in network byte order. Obtain the IP address by calling 
<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>. If this parameter specifies an IP address, the <i>fIsIpAddress</i> parameter should specify a <b>TRUE</b> value.


### -param fIsIpAddress [in]

Specifies a Boolean value that indicates whether the <i>hRasConnection</i> parameter specifies the IP address of the client for which to remove the quarantine filters. If this parameter is a <b>TRUE</b> value, <i>hRasConnection</i> specifies an IP address. Otherwise, <i>hRasConnection</i> specifies a handle to a connection.


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
The handle to the RAS server or the handle to the RAS connection is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The RAS client is not in quarantine.

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



If <a href="https://msdn.microsoft.com/library/ms688288(v=VS.85).aspx">Internet Authentication Service (IAS)</a> policies configure regular filters, then these filters are added to the RAS client interface as a result of calling 
<b>MprAdminConnectionRemoveQuarantine</b>.




## -see-also




<a href="https://msdn.microsoft.com/27be536e-0437-4e30-aef7-ed92f50baeaa">MprAdminConnectionEnum</a>



<a href="https://msdn.microsoft.com/f93b37bc-d3d1-40f0-aef6-839bb43c88e2">MprAdminServerConnect</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 


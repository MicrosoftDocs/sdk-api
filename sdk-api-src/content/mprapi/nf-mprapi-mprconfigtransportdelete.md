---
UID: NF:mprapi.MprConfigTransportDelete
title: MprConfigTransportDelete function
author: windows-sdk-content
description: The MprConfigTransportDelete function removes the specified transport from the list of transports present in the specified router configuration.
old-location: rras\mprconfigtransportdelete.htm
tech.root: RRAS
ms.assetid: e022d0bc-f5ae-4c04-80f7-40ec77e2fa80
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprConfigTransportDelete, MprConfigTransportDelete function [RAS], _mpr_mprconfigtransportdelete, mprapi/MprConfigTransportDelete, rras.mprconfigtransportdelete
ms.topic: function
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
 - MprConfigTransportDelete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigTransportDelete function


## -description


The 
<b>MprConfigTransportDelete</b> function removes the specified transport from the list of transports present in the specified router configuration.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration from which to remove the transport. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param hRouterTransport [in]

Handle to the configuration for the transport being deleted. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/a4cc4519-ce76-4619-b6dc-a5dfa18134e6">MprConfigTransportCreate</a> or 
<a href="https://msdn.microsoft.com/2d3a2300-de10-4ee0-ba0e-bda26cf9a910">MprConfigTransportGetHandle</a>.


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
The <i>hMprConfig</i> parameter is <b>NULL</b>, or the <i>hRouterTransport</i> parameter is <b>NULL</b>, or both are <b>NULL</b>.

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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/a4cc4519-ce76-4619-b6dc-a5dfa18134e6">MprConfigTransportCreate</a>



<a href="https://msdn.microsoft.com/2d3a2300-de10-4ee0-ba0e-bda26cf9a910">MprConfigTransportGetHandle</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 


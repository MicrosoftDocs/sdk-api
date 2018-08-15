---
UID: NF:mprapi.MprConfigInterfaceTransportRemove
title: MprConfigInterfaceTransportRemove function
author: windows-sdk-content
description: The MprConfigInterfaceTransportRemove function removes the specified transport from the specified interface configuration on the router.
old-location: rras\mprconfiginterfacetransportremove.htm
old-project: rras
ms.assetid: 0f286003-f9d8-490b-a379-76baa3f53c6f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MprConfigInterfaceTransportRemove, MprConfigInterfaceTransportRemove function [RAS], _mpr_mprconfiginterfacetransportremove, mprapi/MprConfigInterfaceTransportRemove, rras.mprconfiginterfacetransportremove
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigInterfaceTransportRemove
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigInterfaceTransportRemove function


## -description


The 
<b>MprConfigInterfaceTransportRemove</b> function removes the specified transport from the specified interface configuration on the router.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. The handle is obtained from a previous call to 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param hRouterInterface [in]

Handle to the interface configuration from which to delete the specified transport. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/e368aa3c-bb80-49ed-a1da-39777dada960">MprConfigInterfaceCreate</a>, 
<a href="https://msdn.microsoft.com/1088e587-4446-4463-b411-a11e34adaf6a">MprConfigInterfaceGetHandle</a>, or 
<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>.


### -param hRouterIfTransport [in]

Handle to the interface transport configuration to be deleted. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f4735fd1-031d-4cda-af40-36f55e5796f9">MprConfigInterfaceTransportAdd</a>, 
<a href="https://msdn.microsoft.com/668ad25c-c5a6-4676-825d-310cc99b321b">MprConfigInterfaceTransportGetHandle</a>, or 
<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>. Supported transport protocol types are listed on <a href="https://msdn.microsoft.com/7720c34f-0558-49de-8f82-13a67e2c8c69">Transport Identifiers</a>.


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
One of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b>.</li>
<li><i>hRouterInterface</i> is <b>NULL</b>.</li>
<li><i>phRouterIfTransport</i> is <b>NULL</b>.</li>
</ul>
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
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="_win32_formatmessage">FormatMessage</a>



<a href="https://msdn.microsoft.com/e368aa3c-bb80-49ed-a1da-39777dada960">MprConfigInterfaceCreate</a>



<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>



<a href="https://msdn.microsoft.com/1088e587-4446-4463-b411-a11e34adaf6a">MprConfigInterfaceGetHandle</a>



<a href="https://msdn.microsoft.com/f4735fd1-031d-4cda-af40-36f55e5796f9">MprConfigInterfaceTransportAdd</a>



<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>



<a href="https://msdn.microsoft.com/668ad25c-c5a6-4676-825d-310cc99b321b">MprConfigInterfaceTransportGetHandle</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 


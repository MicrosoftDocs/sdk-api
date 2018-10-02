---
UID: NF:mprapi.MprConfigInterfaceTransportSetInfo
title: MprConfigInterfaceTransportSetInfo function
author: windows-sdk-content
description: The MprConfigInterfaceTransportSetInfo function updates the configuration information for the client on the specified interface and transport protocol.
old-location: rras\mprconfiginterfacetransportsetinfo.htm
tech.root: RRAS
ms.assetid: 1f46b528-d9a1-4967-afa2-424ee1eebbcb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MprConfigInterfaceTransportSetInfo, MprConfigInterfaceTransportSetInfo function [RAS], _mpr_mprconfiginterfacetransportsetinfo, mprapi/MprConfigInterfaceTransportSetInfo, rras.mprconfiginterfacetransportsetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MprConfigInterfaceTransportSetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigInterfaceTransportSetInfo function


## -description


The 
<b>MprConfigInterfaceTransportSetInfo</b> function updates the configuration information for the client on the specified interface and transport protocol.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param hRouterInterface [in]

Handle to the interface configuration in which to update the information. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/e368aa3c-bb80-49ed-a1da-39777dada960">MprConfigInterfaceCreate</a> or 
<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>.


### -param hRouterIfTransport [in]

Handle to the transport configuration in which to update the information for the client. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f4735fd1-031d-4cda-af40-36f55e5796f9">MprConfigInterfaceTransportAdd</a>, 
<a href="https://msdn.microsoft.com/668ad25c-c5a6-4676-825d-310cc99b321b">MprConfigInterfaceTransportGetHandle</a>, or 
<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>. Supported transport protocol types are listed on <a href="https://msdn.microsoft.com/7720c34f-0558-49de-8f82-13a67e2c8c69">Transport Identifiers</a>.


### -param pInterfaceInfo [in, optional]

Pointer to an information header that contains configuration information for the client on the specified interface and transport. The router manager for the specified transport interprets this information. Use the 
<a href="https://msdn.microsoft.com/e88720aa-080b-4d87-a442-1b436c256ca6">Information Header Functions</a> to manipulate information headers. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not update the configuration information for the client.


### -param dwInterfaceInfoSize [in, optional]

Specifies the size, in bytes, of the data pointed to by <i>pInterfaceInfo</i>. 




This parameter is optional; the calling application may specify zero for this parameter. However, if <i>pInterfaceInfo</i> is not <b>NULL</b>, this parameter cannot be zero. For more information, see the Remarks section later in this topic.


## -returns



If the function succeeds, the return value is NO_ERROR. For more information, see the Remarks section later in this topic.

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
<li><i>hRouterInterface</i> is <b>NULL</b>.</li>
<li><i>hRouterIfTransport</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_INTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The interface specified by <i>hRouterInterface</i> is no longer present in the router configuration, or the transport specified by <i>hRouterInterface</i> is no longer present on the interface.

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
 




## -remarks



If the <i>pInterfaceInfo</i> parameter is <b>NULL</b>, 
<b>MprConfigInterfaceTransportSetInfo</b> does nothing and returns immediately with a value of NO_ERROR.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/e368aa3c-bb80-49ed-a1da-39777dada960">MprConfigInterfaceCreate</a>



<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>



<a href="https://msdn.microsoft.com/1088e587-4446-4463-b411-a11e34adaf6a">MprConfigInterfaceGetHandle</a>



<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>



<a href="https://msdn.microsoft.com/668ad25c-c5a6-4676-825d-310cc99b321b">MprConfigInterfaceTransportGetHandle</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 


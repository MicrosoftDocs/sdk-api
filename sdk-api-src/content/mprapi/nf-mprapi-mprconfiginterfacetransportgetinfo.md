---
UID: NF:mprapi.MprConfigInterfaceTransportGetInfo
title: MprConfigInterfaceTransportGetInfo function
author: windows-driver-content
description: The MprConfigInterfaceTransportGetInfo function retrieves the configuration information for the specified client on the specified interface.
old-location: rras\mprconfiginterfacetransportgetinfo.htm
old-project: RRAS
ms.assetid: 2b0bb412-a480-43ff-b29a-cf4e7674d2c4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MprConfigInterfaceTransportGetInfo, MprConfigInterfaceTransportGetInfo function [RAS], _mpr_mprconfiginterfacetransportgetinfo, mprapi/MprConfigInterfaceTransportGetInfo, rras.mprconfiginterfacetransportgetinfo
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprConfigInterfaceTransportGetInfo
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprConfigInterfaceTransportGetInfo function


## -description


The 
<b>MprConfigInterfaceTransportGetInfo</b> function retrieves the configuration information for the specified client on the specified interface.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param hRouterInterface [in]

Handle to the interface configuration from which to retrieve the specified client information. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/e368aa3c-bb80-49ed-a1da-39777dada960">MprConfigInterfaceCreate</a>, 
<a href="https://msdn.microsoft.com/1088e587-4446-4463-b411-a11e34adaf6a">MprConfigInterfaceGetHandle</a>, or 
<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>.


### -param hRouterIfTransport [in]

Handle to the transport configuration from which to retrieve the specified client information. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/f4735fd1-031d-4cda-af40-36f55e5796f9">MprConfigInterfaceTransportAdd</a>, 
<a href="https://msdn.microsoft.com/668ad25c-c5a6-4676-825d-310cc99b321b">MprConfigInterfaceTransportGetHandle</a>, or 
<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>. Supported transport protocol types are listed on <a href="https://msdn.microsoft.com/7720c34f-0558-49de-8f82-13a67e2c8c69">Transport Identifiers</a>.


### -param ppInterfaceInfo [in, out, optional]

On input, pointer to a pointer variable. 




On output, this pointer variable points to an information header that contains configuration information for the client. Use the 
<a href="https://msdn.microsoft.com/e88720aa-080b-4d87-a442-1b436c256ca6">Information Header Functions</a> to manipulate information headers. Free this memory by calling 
<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>.

This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return the configuration information.


### -param lpdwInterfaceInfoSize [out, optional]

Pointer to a <b>DWORD</b> variable. This variable receives the size, in bytes, of the data pointed to by <i>ppInterfaceInfo</i>. 




This parameter is optional; the calling application may specify <b>NULL</b> for this parameter. However, if <i>ppInterfaceInfo</i> is not <b>NULL</b>, this parameter cannot be <b>NULL</b>. For more information, see the Remarks section later in this topic.


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
One of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b>.</li>
<li><i>hRouterInterface</i> is <b>NULL</b>.</li>
<li><i>hRouterIfTransport</i> is <b>NULL</b>.</li>
<li><i>ppInterfaceInfo</i> is not <b>NULL</b>, but <i>lpdwInterfaceInfoSize</i> is <b>NULL</b>.</li>
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
The interface specified by <i>hRouterIfTransport</i> was not found in the router configuration, or the transport specified by <i>hRouterIfTransport</i> was not enabled on the specified interface.

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
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 


<div> </div>





## -remarks



If the <i>ppInterfaceInfo</i> parameter is <b>NULL</b>, 
<b>MprConfigInterfaceTransportGetInfo</b> does nothing and returns immediately with a value of NO_ERROR.




## -see-also




<a href="_win32_formatmessage">FormatMessage</a>



<a href="https://msdn.microsoft.com/4ee360be-fe5f-477e-901f-92d083f68451">MPR_IFTRANSPORT_0</a>



<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>



<a href="https://msdn.microsoft.com/e368aa3c-bb80-49ed-a1da-39777dada960">MprConfigInterfaceCreate</a>



<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>



<a href="https://msdn.microsoft.com/1088e587-4446-4463-b411-a11e34adaf6a">MprConfigInterfaceGetHandle</a>



<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>



<a href="https://msdn.microsoft.com/668ad25c-c5a6-4676-825d-310cc99b321b">MprConfigInterfaceTransportGetHandle</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 


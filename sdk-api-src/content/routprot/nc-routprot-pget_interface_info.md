---
UID: NC:routprot.PGET_INTERFACE_INFO
title: PGET_INTERFACE_INFO
author: windows-sdk-content
description: The GetInterfaceInfo function gets the configuration information kept by the routing protocol for a specific interface.
old-location: rras\getinterfaceinfo.htm
old-project: RRAS
ms.assetid: ec662772-f864-4108-b676-3fa501b3b927
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetInterfaceInfo, PGET_INTERFACE_INFO, PGET_INTERFACE_INFO callback, PGET_INTERFACE_INFO callback function [RAS], _mpr_getinterfaceinfo, routprot/PGET_INTERFACE_INFO, rras.getinterfaceinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: routprot.h
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Routprot.h
api_name:
-	PGET_INTERFACE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PGET_INTERFACE_INFO callback function


## -description


The 
<b>GetInterfaceInfo</b> function gets the configuration information kept by the routing protocol for a specific interface.


## -parameters




### -param InterfaceIndex [in]

Specifies the interface in the set of interfaces configured on the router.


### -param InterfaceInfo [in]

Pointer to a buffer that receives the protocol-defined configuration information associated with the interface. This information is private to the routing protocol.


### -param BufferSize [in, out]

Pointer to a <b>DWORD</b> variable. 




On input: This variable specifies the size, in bytes, of the buffer provided to receive the configuration information.

On output: This variable receives the size, in bytes, of the data placed in the buffer. If the initial size was not large enough, this variable contains the size required to hold all of the data.


### -param StructureVersion [in]

Specifies the version of the information structures pointed to by the <i>InterfaceInfo</i> parameter. In some cases, this is equal to the version of the routing protocol.


### -param StructureSize [in]

Specifies the size of each of the information structures pointed to by the <i>InterfaceInfo</i> parameter. Since some information structures contain variable length members, the routing protocol isn't necessarily able to determine the size of the information from the version.


### -param StructureCount [in]

Specifies a count of the number of information structures pointed to by the <i>InterfaceInfo</i> parameter. This parameter is always one.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The attempt to retrieve the information failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>InterfaceIndex</i> parameter is invalid (for example, no interface exists with that index), or the <i>InterfaceInfoSize</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the output buffer provided is not large enough to hold the requested information. The required size is returned in the <b>DWORD</b> variable pointed to by <i>InterfaceInfoSize</i>.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/fd780458-ef23-4ef2-8fe8-29b32100917f">Routing Protocol Interface Functions</a>



<a href="https://msdn.microsoft.com/0429f5ca-6574-48f5-85ab-70b4677ca539">Routing Protocol Interface Reference</a>



<a href="https://msdn.microsoft.com/abcfa220-a860-48cc-92c5-60ce655678b7">SetInterfaceInfo</a>
 

 


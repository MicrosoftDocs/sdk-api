---
UID: NC:routprot.PGET_NEIGHBORS
title: PGET_NEIGHBORS (routprot.h)
author: windows-sdk-content
description: The router manager calls the GetNeighbors function to obtain the querier for the network attached through the specified interface.
old-location: rras\getneighbors.htm
tech.root: RRAS
ms.assetid: 31a28a43-3cfd-4d3c-813e-8f8289d99712
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNeighbors, GetNeighbors callback function [RAS], PGET_NEIGHBORS, PGET_NEIGHBORS callback, _mpr_getneighbors, routprot/GetNeighbors, rras.getneighbors
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - GetNeighbors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PGET_NEIGHBORS callback function


## -description


The router manager calls the 
<i>GetNeighbors</i> function to obtain the querier for the network attached through the specified interface.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PGET_NEIGHBORS</a> type defines a pointer to this callback function. <i>GetNeighbors</i> is a placeholder for the application-defined function name.


## -parameters




### -param InterfaceIndex [in]

Specifies the index of the interface on which the routing protocol should provide the querier.


### -param NeighborList [in]

Pointer to an array <b>DWORD</b> variables. The routing protocol should fill in this array with the address of the querier. 




If the local computer is the querier for the network attached through the specified interface, the routing protocol need not fill in this variable. Instead, the routing protocol should set the value pointed to by <i>NeighborListSize</i> to zero. Also, the routing protocol should add <b>MRINFO_QUERIER_FLAG</b> to the flags returned in the <i>InterfaceFlags</i> parameter.


### -param NeighborListSize [in, out]

On input, pointer to a <b>DWORD</b> variable. 




On output, the routing protocol fills this variable with the length, in bytes, of the address returned in the <i>NeighborList</i> parameter.


### -param InterfaceFlags [out]

Receives one or more of the following flags. The flags describe the relationship of the local computer to other computers on the network attached through the specified interface. 




<b>MRINFO_TUNNEL_FLAG</b>
<b>MRINFO_PIM_FLAG</b>
<b>MRINFO_DOWN_FLAG</b>
<b>MRINFO_DISABLED_FLAG</b>
<b>MRINFO_QUERIER_FLAG</b>
<b>MRINFO_LEAF_FLAG</b>

## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

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
The routing protocol could not complete the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The size of the buffer pointed to by <i>NeighborList</i> is not large enough to hold the address. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>NeighborListSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>InterfaceIndex</i> parameter is invalid (for example, no interface exists with that index).

</td>
</tr>
</table>
 




## -remarks



Only multicast routing protocols are required implement this function. Non-multicast routing protocols should pass <b>NULL</b> as the pointer value for this function in 
<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a>





## -see-also




<a href="https://msdn.microsoft.com/518eb335-13b9-4980-90fc-11cdd7ef8f1a">GetMfeStatus</a>
 

 


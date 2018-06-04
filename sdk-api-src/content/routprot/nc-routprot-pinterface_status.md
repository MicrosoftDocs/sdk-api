---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PINTERFACE_STATUS callback function


## -description


Router manager calls the 
<b>InterfaceStatus</b> function to change the status of an interface.

The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PINTERFACE_STATUS</a> type defines a pointer to this callback function. <i>InterfaceStatus</i> is a placeholder for the application-defined function name.


## -parameters




### -param InterfaceIndex [in]

Specifies the index of the interface to change.


### -param InterfaceActive [in]

Specifies whether the interface is active.


### -param StatusType [in]

Specifies the new interface status. This parameter is one of the following values. 




RIS_INTERFACE_ADDRESS_CHANGE

RIS_INTERFACE_ENABLED

RIS_INTERFACE_DISABLED

RIS_INTERFACE_MEDIA_PRESENT

RIS_INTERFACE_MEDIA_ABSENT


### -param StatusInfo [in]

Pointer to a structure that specifies information appropriate to the type of interface status type. For example, if the <i>StatusType</i> parameter specifies an address change, the <i>StatusInfo</i> parameter  points to a structure that contains the new address information, such as 
<a href="https://msdn.microsoft.com/3eb864e7-2de6-44c2-af3e-fee547de6081">IP_ADAPTER_BINDING_INFO</a>. This parameter may be <b>NULL</b>.


## -returns



If the function succeeds, the return value should be NO_ERROR.

If the function fails, the return value should be one of the following error codes.

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
Unspecified failure.

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
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/d2a90d20-7a1f-4301-adab-76224a4f8310">AddInterface</a>



<a href="https://msdn.microsoft.com/0b4c24d4-2588-412e-b3ec-dd73cbdac921">DeleteInterface</a>
 

 


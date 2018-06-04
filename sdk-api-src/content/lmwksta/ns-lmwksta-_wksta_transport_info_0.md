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

# _WKSTA_TRANSPORT_INFO_0 structure


## -description


The 
				<b>WKSTA_TRANSPORT_INFO_0</b> structure contains information about the workstation transport protocol, such as Wide Area Network (WAN) or NetBIOS.


## -struct-fields




### -field wkti0_quality_of_service

Specifies a value that determines the search order of the transport protocol with respect to other transport protocols. The highest value is searched first.


### -field wkti0_number_of_vcs

Specifies the number of clients communicating with the server using this transport protocol.


### -field wkti0_transport_name

Specifies the device name of the transport protocol.


### -field wkti0_transport_address

Specifies the address of the server on this transport protocol.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -field wkti0_wan_ish

This member is ignored by the 
<a href="https://msdn.microsoft.com/016060ea-eae1-421f-b708-5c2ddd2000c1">NetWkstaTransportAdd</a> function. For the 
<a href="https://msdn.microsoft.com/08bd22a9-00a7-4563-9353-c070ca9b2500">NetWkstaTransportEnum</a> function, this member indicates whether the transport protocol is a WAN transport protocol. This member is set to <b>TRUE</b> for NetBIOS/TCIP; it is set to <b>FALSE</b> for NetBEUI and NetBIOS/IPX. 




Certain legacy networking protocols, including NetBEUI, will no longer be supported. For more information, see 
<a href="https://msdn.microsoft.com/8c123e09-b11a-4c92-b41e-49cc01be53d3">Network Protocol Support in Windows</a>.


## -see-also




<a href="https://msdn.microsoft.com/016060ea-eae1-421f-b708-5c2ddd2000c1">NetWkstaTransportAdd</a>



<a href="https://msdn.microsoft.com/08bd22a9-00a7-4563-9353-c070ca9b2500">NetWkstaTransportEnum</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/64342e21-98f1-42d3-b541-46b826391fad">Server and Workstation Transport Functions</a>
 

 


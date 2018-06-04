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

# IPSEC_VIRTUAL_IF_TUNNEL_INFO0_ structure


## -description


The <b>IPSEC_VIRTUAL_IF_TUNNEL_INFO0</b> structure is used to store information specific to virtual interface tunneling.


## -struct-fields




### -field virtualIfTunnelId

ID of the  virtual interface tunnel state.


### -field trafficSelectorId

ID of the virtual interface tunneling traffic selector(s).


## -remarks



 The <b>IPSEC_VIRTUAL_IF_TUNNEL_INFO0</b> structure is applicable only to Internet Key Exchange version 2 (IKEv2).

<b>IPSEC_VIRTUAL_IF_TUNNEL_INFO0</b> is a specific implementation of IPSEC_VIRTUAL_IF_TUNNEL_INFO. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 


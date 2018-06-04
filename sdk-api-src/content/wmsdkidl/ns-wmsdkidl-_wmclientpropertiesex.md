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

# _WMClientPropertiesEx structure


## -description



The <b>WM_CLIENT_PROPERTIES_EX </b>structure holds extended client information.




## -struct-fields




### -field cbSize

<b>DWORD</b> containing the size of the structure.


### -field pwszIPAddress

String containing the client's IP address in dot notation (for example, "192.168.10.2").


### -field pwszPort

String containing the client's port number.


### -field pwszDNSName

String containing the client's name on the domain name server (DNS), if known.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>



<a href="https://msdn.microsoft.com/62a5bafd-cc49-4a60-be03-038920e5b073">WM_CLIENT_PROPERTIES</a>
 

 


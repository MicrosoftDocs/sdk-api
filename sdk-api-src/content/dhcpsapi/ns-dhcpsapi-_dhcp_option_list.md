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

# _DHCP_OPTION_LIST structure


## -description


The <b>DHCP_OPTION_LIST</b> structure defines a list of DHCP option values (just the option data  with associated ID tags).


## -struct-fields




### -field NumOptions

Specifies the number of option values  listed in <b>Options</b>.


### -field Options

Pointer to a list of <a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">DHCP_OPTION_VALUE</a> structures


### -field Options.size_is

 


### -field Options.size_is.NumOptions

 




## -see-also




<a href="https://msdn.microsoft.com/6a11cb60-2690-45d4-a5e6-a3ebdc1efe3d">DHCP_OPTION_VALUE</a>



<a href="https://msdn.microsoft.com/60f4db5f-0359-4738-980e-2a56adbf551e">DhcpGetClientOptions</a>
 

 


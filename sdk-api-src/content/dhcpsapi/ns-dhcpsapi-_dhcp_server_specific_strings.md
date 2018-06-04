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

# _DHCP_SERVER_SPECIFIC_STRINGS structure


## -description


The <b>DHCP_SERVER_SPECIFIC_STRINGS</b> structure contains the default string values for user and vendor class names.


## -struct-fields




### -field DefaultVendorClassName

Pointer to a Unicode string that specifies the default vendor class name for the DHCP server.


### -field DefaultUserClassName

Pointer to a Unicode string that specifies the default user class name for the DHCP server.


## -see-also




<a href="https://msdn.microsoft.com/dc283fa3-6077-4010-8c71-9dc91ed2dadf">DhcpGetServerSpecificStrings</a>
 

 


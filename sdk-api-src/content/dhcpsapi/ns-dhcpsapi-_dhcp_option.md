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

# _DHCP_OPTION structure


## -description


The <b>DHCP_OPTION</b> structure defines a single DHCP option and any data elements associated with it.


## -struct-fields




### -field OptionID


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_OPTION_ID</a> value that specifies a unique ID number (also called a "code") for this option.


### -field OptionName

Unicode string that contains the name of this option.


### -field OptionComment

Unicode string that contains a comment about this option.


### -field DefaultValue


<a href="https://msdn.microsoft.com/6b2e5866-f65f-4ff0-a531-3d07b972f55e">DHCP_OPTION_DATA</a> structure that contains the data associated with this option.


### -field OptionType


<a href="https://msdn.microsoft.com/2577c0b6-aa84-4176-87b7-ffd304823d76">DHCP_OPTION_TYPE</a> enumeration value that indicates whether this option is a single unary item or an element in an array of options.


## -see-also




<a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a>



<a href="https://msdn.microsoft.com/6b2e5866-f65f-4ff0-a531-3d07b972f55e">DHCP_OPTION_DATA</a>



<a href="https://msdn.microsoft.com/2577c0b6-aa84-4176-87b7-ffd304823d76">DHCP_OPTION_TYPE</a>
 

 


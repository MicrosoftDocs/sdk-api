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

# _DHCP_CLASS_INFO_ARRAY_V6 structure


## -description


The <b>DHCP_CLASS_INFO_ARRAY_V6</b> structure contains a list of information regarding a user class or a vendor class.




## -struct-fields




### -field NumElements

This is of type <b>DWORD</b>, specifying the number of classes whose information is contained in the array specified by Classes.


### -field Classes

A pointer to an array of structures <a href="https://msdn.microsoft.com/76d9a46b-6958-4c29-8512-e6299b28ca01">DHCP_CLASS_INFO_V6</a> (section 2.2.1.2.70) that contains information regarding the various user classes and vendor classes.


### -field Classes.size_is

 


### -field Classes.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/76d9a46b-6958-4c29-8512-e6299b28ca01">DHCP_CLASS_INFO_V6</a>
 

 


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

# SdpQueryUuidUnion structure


## -description


The <b>SdpQueryUuidUnion</b> union contains the UUID on which to perform an SDP query. Used in conjunction with the <b>SdpQueryUuid</b> structure.


## -struct-fields




### -field uuid128

UUID in 128-bit format.


### -field uuid128.case

 


### -field uuid128.case.SDP_ST_UUID128

 


### -field uuid32

UUID in 32-bit format.


### -field uuid32.case

 


### -field uuid32.case.SDP_ST_UUID32

 


### -field uuid16

UUID in 16-bit format.


### -field uuid16.case

 


### -field uuid16.case.SDP_ST_UUID16

 


### -field switch_type

 


### -field switch_type.unsigned short

 




## -see-also




<a href="https://msdn.microsoft.com/b208b7d6-305c-4acc-9c89-75721ff5dcb2">BTH_QUERY_SERVICE</a>



<a href="https://msdn.microsoft.com/8c67b1b1-d289-4273-a512-589b19cd1f85">SdpQueryUuid</a>
 

 


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

# _CLASS_MEDIA_CHANGE_CONTEXT structure


## -description


Contains information associated with a media change event.


## -struct-fields




### -field MediaChangeCount

The number of times that media has been changed since system startup.


### -field NewState

The state information. This member can be one of the following values from the 
      <b>MEDIA_CHANGE_DETECTION_STATE</b> enumeration type.



#### MediaUnknown (0)



#### MediaPresent (1)



#### MediaNotPresent (2)



#### MediaUnavailable (3)


## -see-also




<a href="https://msdn.microsoft.com/6e66fa93-0cd7-4202-83eb-cddc668525ae">DBT_CUSTOMEVENT</a>



<a href="https://msdn.microsoft.com/e25d35b9-f8f1-4850-996c-e1cb393cca66">DBT_DEVICEREMOVECOMPLETE</a>
 

 


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

# USN_RANGE_TRACK_OUTPUT structure


## -description


Contains returned update sequence number (USN) from <a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a> control code.


## -struct-fields




### -field Usn

Returned update sequence number (USN) that identifies at what point in the USN Journal that range tracking was enabled.


## -remarks



This structure is optional.




## -see-also




<a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a>
 

 


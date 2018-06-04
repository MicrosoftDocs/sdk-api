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

# IRDPSRAPISharingSession::GetDesktopSharedRect


## -description


Retrieves the current desktop region being shared.


## -parameters




### -param pleft




### -param ptop




### -param pright




### -param pbottom






#### - bottom [out]

Type: <b>long*</b>

Y-coordinate of the lower-right corner of the shared rectangle.


#### - left [out]

Type: <b>long*</b>

X-coordinate of the upper-left corner of the shared rectangle.


#### - right [out]

Type: <b>long*</b>

X-coordinate of the lower-right corner of the shared rectangle.


#### - top [out]

Type: <b>long*</b>

Y-coordinate of the upper-left corner of the shared rectangle.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/531382ec-d94f-411e-bd43-86cd3066ac26">IRDPSRAPISharingSession</a>



<a href="https://msdn.microsoft.com/3ac68be7-e6fd-42c7-b2f3-b90bb5097b07">IRDPSRAPISharingSession2</a>
 

 


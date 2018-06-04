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

# IDiscRecorder::QueryMediaInfo


## -description


Retrieves information about the currently mounted media, such as the total number of blocks used on the media.


## -parameters




### -param pbSessions




### -param pbLastTrack




### -param ulStartAddress




### -param ulNextWritable




### -param ulFreeBlocks






#### - pblasttrack [out]

Track number of the last track of the previous session.


#### - pbsessions [out]

Number of sessions on the disc.


#### - ulfreeblocks [out]

Number of blocks available for writing.


#### - ulnextwritable [out]

Address at which writing is to begin.


#### - ulstartaddress [out]

Start address of the last track of the previous session.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Using this method allows the calculation of parameters such as the amount of free space left on the disc without using a setting on the active disc recorder, which causes an exclusive open. The total size of the disc can be calculated by summing the next writable address and free blocks.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 


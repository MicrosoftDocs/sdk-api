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

# _CSV_IS_OWNED_BY_CSVFS structure


## -description


Contains the output for the 
    <a href="https://msdn.microsoft.com/AA9D31DD-352C-4509-A5F3-55DC1C685E33">FSCTL_IS_VOLUME_OWNED_BYCSVFS</a> control code 
    that determines whether a volume is owned by CSVFS.


## -struct-fields




### -field OwnedByCSVFS

<b>TRUE</b> if a volume is owned by CSVFS; otherwise, 
      <b>FALSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/AA9D31DD-352C-4509-A5F3-55DC1C685E33">FSCTL_IS_VOLUME_OWNED_BYCSVFS</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 


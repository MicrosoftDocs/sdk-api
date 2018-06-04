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

# _FILE_IO_PRIORITY_HINT_INFO structure


## -description


Specifies the priority hint for a file I/O operation.


## -struct-fields




### -field PriorityHint

The priority hint. This member is a value from the 
      <a href="https://msdn.microsoft.com/768e563a-5ff5-4dd2-8811-0a823c253a31">PRIORITY_HINT</a> enumeration.


## -remarks



The <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a> function 
    can be used with this structure to associate a priority hint with I/O operations on a file-handle basis. In 
    addition to the idle priority (very low), this function allows normal priority and low priority. Whether these 
    priorities are supported and honored by the underlying drivers depends on their implementation (which is why they 
    are called hints). For more information, see the 
    <a href="Http://go.microsoft.com/fwlink/p/?linkid=98562">I/O Prioritization in Windows Vista</a> 
    white paper on the Windows Hardware Developer Central (WHDC) website.

This structure must be aligned on a <b>LONGLONG</b> (8-byte) boundary.




## -see-also




<a href="https://msdn.microsoft.com/768e563a-5ff5-4dd2-8811-0a823c253a31">PRIORITY_HINT</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 


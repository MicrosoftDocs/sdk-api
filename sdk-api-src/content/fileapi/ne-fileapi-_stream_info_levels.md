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

# _STREAM_INFO_LEVELS enumeration


## -description


Defines values that are used with the 
    <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> function to specify the information 
    level of the returned data.


## -enum-fields




### -field FindStreamInfoStandard

The <a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a> function retrieves standard 
      stream information. The data is returned in a 
      <a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a> structure.


### -field FindStreamInfoMaxInfoLevel

Used to determine valid enumeration values. All supported enumeration values are less than 
      <b>FindStreamInfoMaxInfoLevel</b>.


## -see-also




<a href="https://msdn.microsoft.com/aab3af94-a2e0-45ad-a846-f457408a19d5">FindFirstStreamW</a>



<a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a>
 

 


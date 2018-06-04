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

# _WTSINFOEXA structure


## -description


Contains a <a href="https://msdn.microsoft.com/d3df1f40-698b-43ca-808d-0df5550b6eae">WTSINFOEX_LEVEL</a> union that contains extended information about a Remote Desktop Services session. This structure is returned by the <a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a> function when you specify "WTSSessionInfoEx" for the <i>WTSInfoClass</i> parameter.


## -struct-fields




### -field Level

Specifies the level  of information contained in the <b>Data</b> member. This can be the following value.



#### 1

The <b>Data</b> member is a <a href="https://msdn.microsoft.com/bad4f35a-04a9-42fa-b87e-0f51e9f0f30e">WTSINFOEX_LEVEL1</a> structure.


### -field Data

A <a href="https://msdn.microsoft.com/d3df1f40-698b-43ca-808d-0df5550b6eae">WTSINFOEX_LEVEL</a> union. The type of structure contained here is specified by the <b>Level</b> member.


## -see-also




<a href="https://msdn.microsoft.com/d3df1f40-698b-43ca-808d-0df5550b6eae">WTSINFOEX_LEVEL</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>
 

 


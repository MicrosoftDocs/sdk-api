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

# tagMULTIKEYHELPW structure


## -description


Specifies a keyword to search for and the keyword table to be searched by Windows Help.


## -struct-fields




### -field mkSize

Type: <b>DWORD</b>

The structure size, in bytes.


### -field mkKeylist

Type: <b>TCHAR</b>

A single character that identifies the keyword table to search.


### -field szKeyphrase

Type: <b>TCHAR[1]</b>

A null-terminated text string that specifies the keyword to locate in the keyword table.


## -see-also




<a href="https://msdn.microsoft.com/fce80bac-2a44-46e7-a87a-ef93f4599807">WinHelp</a>
 

 


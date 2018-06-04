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

# tagAAMENUFILENAME structure


## -description


A variable-size structure that contains information about a menu file name.


## -struct-fields




### -field cbTotal

Type: <b>SHORT</b>

The size of the structure, in bytes.


### -field rgbReserved

Type: <b>BYTE[12]</b>

Reserved. Applications should ignore this value.


### -field szFileName

Type: <b>TCHAR[1]</b>

The menu file name. This string is in Unicode on Windows 2000.


## -remarks



<div class="alert"><b>Important</b>  This structure cannot be used with operating systems later than Windows 2000.</div>
<div> </div>
When reading an <b>AASHELLMENUFILENAME</b> structure, first read a single SHORT to determine the total size of the structure, then use that value to read the remainder of the structure.




## -see-also




<a href="https://msdn.microsoft.com/9d5ccbae-cc56-446f-be67-9623247d5045">AASHELLMENUITEM</a>
 

 


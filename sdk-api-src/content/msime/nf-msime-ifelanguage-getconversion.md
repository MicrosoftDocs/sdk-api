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

# IFELanguage::GetConversion


## -description


Converts the input string (which usually contains the Hiragana character) to converted strings.


## -parameters




### -param string [in]

A string of phonetic characters to convert.


### -param start [in]

The starting character from which <a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a> begins conversion. The first character of <i>string</i> is represented by 1 (not 0).


### -param length [in]

The number of characters to convert. If this value is -1, all of the remaining characters from <i>start</i>  are converted.


### -param result [out, retval]

The converted string. This string is allocated by <a href="https://msdn.microsoft.com/f98bff39-bc5f-4a81-85d7-d5228e20fbc8">SysAllocStringLen</a> and must be freed by the client.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a>
 

 


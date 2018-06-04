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

# StringFromCLSID function


## -description


Converts a CLSID into a string of printable characters. Different CLSIDs always convert to different strings.




## -parameters




### -param rclsid [in]

The CLSID to be converted.


### -param lplpsz [out]

The address of a pointer variable that receives a pointer to the resulting string. The string that represents <i>rclsid</i> includes enclosing braces.


## -returns



This function can return the standard return values E_OUTOFMEMORY and S_OK.




## -remarks



<b>StringFromCLSID</b> calls the <a href="https://msdn.microsoft.com/5f437658-b749-416b-805a-2afdac682660">StringFromGUID2</a> function to convert a globally unique identifier (GUID) into a string of printable characters.

The caller is responsible for freeing the memory allocated for the string by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function. 





## -see-also




<a href="https://msdn.microsoft.com/36cc9037-480f-491f-a9bb-5aa1e707781e">CLSIDFromString</a>



<a href="https://msdn.microsoft.com/5f437658-b749-416b-805a-2afdac682660">StringFromGUID2</a>
 

 


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

# SetupDiGetClassDescriptionW function


## -description


The <b>SetupDiGetClassDescription</b> function retrieves the class description associated with the specified setup class GUID.


## -parameters




### -param ClassGuid [in]

The GUID of the setup class whose description is to be retrieved.


### -param ClassDescription [out]

A pointer to a character buffer that receives the class description.


### -param ClassDescriptionSize [in]

The size, in characters, of the <i>ClassDescription</i> buffer.


### -param RequiredSize [out, optional]

A pointer to variable of type DWORD that receives the size, in characters, that is required to store the class description (including a NULL terminator). <i>RequiredSize</i> is always less than LINE_LEN. This parameter is optional and can be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Call <b>SetupDiGetClassDescriptionEx</b> to retrieve the description of a setup class installed on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550909">SetupDiBuildClassInfoList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551058">SetupDiGetClassDescriptionEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552010">SetupDiGetINFClass</a>
 

 


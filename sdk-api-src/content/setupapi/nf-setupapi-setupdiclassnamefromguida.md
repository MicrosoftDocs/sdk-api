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

# SetupDiClassNameFromGuidA function


## -description


The <b>SetupDiClassNameFromGuid</b> function retrieves the class name associated with a class GUID.


## -parameters




### -param ClassGuid [in]

A pointer to the class GUID for the class name to retrieve.


### -param ClassName [out]

A pointer to a buffer that receives the NULL-terminated string that contains the name of the class that is specified by the pointer in the <i>ClassGuid</i> parameter.


### -param ClassNameSize [in]

The size, in characters, of the buffer that is pointed to by the <i>ClassName</i> parameter. The maximum size, in characters, of a NULL-terminated class name is MAX_CLASS_NAME_LEN. For more information about the class name size, see the following <b>Remarks</b> section.


### -param RequiredSize [out, optional]

A pointer to a variable that receives the number of characters that are required to store the requested NULL-terminated class name. This pointer is optional and can be <b>NULL</b>. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Call <b>SetupDiClassNameFromGuidEx</b> to retrieve the name for a class on a remote computer.

<b>SetupDiClassNameFromGuid</b> does not enforce a restriction on the length of the class name that it can return. This function returns the required size for a NULL-terminated class name even if it is greater than MAX_CLASS_NAME_LEN. However, MAX_CLASS_NAME_LEN is the maximum length of a valid NULL-terminated class name. A caller should never need a buffer that is larger than MAX_CLASS_NAME_LEN. For more information about class names, see the description of the <b>Class</b> entry of an <a href="https://msdn.microsoft.com/53e30950-28a3-4ae3-a351-a917b02c84a5">INF Version section</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550937">SetupDiClassGuidsFromName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550950">SetupDiClassNameFromGuidEx</a>
 

 


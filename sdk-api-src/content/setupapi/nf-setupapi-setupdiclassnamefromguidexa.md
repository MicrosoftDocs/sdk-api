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

# SetupDiClassNameFromGuidExA function


## -description


The <b>SetupDiClassNameFromGuidEx</b> function retrieves the class name associated with a class GUID. The class can be installed on a local or remote computer.


## -parameters




### -param ClassGuid [in]

The class GUID of the class name to retrieve.


### -param ClassName [out]

A pointer to a string buffer that receives the NULL-terminated name of the class for the specified GUID.


### -param ClassNameSize [in]

The size, in characters, of the <i>ClassName</i> buffer.


### -param RequiredSize [out, optional]

The number of characters required to store the class name (including a terminating null). <i>RequiredSize</i> is always less than MAX_CLASS_NAME_LEN.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system on which the class is installed. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the local system name is used.


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550941">SetupDiClassGuidsFromNameEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550947">SetupDiClassNameFromGuid</a>
 

 


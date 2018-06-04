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

# SetupDiGetClassDescriptionExW function


## -description


The <b>SetupDiGetClassDescriptionEx</b> function retrieves the description of a setup class installed on a local or remote computer.


## -parameters




### -param ClassGuid [in]

A pointer to the GUID for the setup class whose description is to be retrieved.


### -param ClassDescription [out]

A pointer to a character buffer that receives the class description.


### -param ClassDescriptionSize [in]

The size, in characters, of the buffer that is pointed to by the <i>ClassDescription</i> parameter. The maximum length, in characters, of a NULL-terminated class description is LINE_LEN. For more information, see the following <b>Remarks</b> section. 


### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives the size, in characters, that is required to store the requested NULL-terminated class description. This pointer is optional and can be <b>NULL</b>.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that supplies the name of a remote computer on which the setup class resides. This pointer is optional and can be <b>NULL</b>. If the class is installed on a local computer, set the pointer to <b>NULL</b>. 


### -param Reserved

Reserved for system use. A caller of this function must set this parameter to <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If there is a friendly name in the registry key for the class, this routine returns the friendly name. Otherwise, this routine returns the class name.

<b>SetupDiGetClassDescriptionEx</b> does not enforce a restriction on the length of the class description that it can return. This function returns the required size for a NULL-terminated class description even if it is greater than LINE_LEN. However, LINE_LEN is the maximum length of a valid NULL-terminated class description. A caller should never need a buffer that is larger than LINE_LEN. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550909">SetupDiBuildClassInfoList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550911">SetupDiBuildClassInfoListEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551103">SetupDiGetDeviceInfoListDetail</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552010">SetupDiGetINFClass</a>
 

 


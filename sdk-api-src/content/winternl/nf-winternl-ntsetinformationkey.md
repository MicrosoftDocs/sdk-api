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

# NtSetInformationKey function


## -description


<p class="CCE_Message">[This function may be changed or removed from Windows without further notice.]

Sets information for the specified registry key.


## -parameters




### -param KeyHandle [in]

A handle to the registry key. The handle must be opened with the <b>KEY_WRITE</b> access 
      right.


### -param KeySetInformationClass [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553399">KEY_SET_INFORMATION_CLASS</a> value that 
      specifies the kind of information to be set.


### -param KeySetInformation [in]

A pointer to the buffer that contains the information to be set. The format of this buffer is determined by 
      the <i>KeySetInformationClass</i> parameter.


### -param KeySetInformationLength [in]

The length of the buffer specified by the <i>KeySetInformation</i> parameter, in 
      bytes.


## -returns



Returns an <b>NTSTATUS</b> or error code. An error code of 
       <b>STATUS_INFO_LENGTH_MISMATCH</b> indicates that the 
       <i>KeySetInformationLength</i> parameter is the wrong length for the information class 
       specified by the <i>KeySetInformationClass</i> parameter.

The forms and significance of <b>NTSTATUS</b> error codes are listed in the Ntstatus.h 
       header file available in the WDK, and are described in the WDK documentation.




## -remarks



The associated import library, Ntdll.lib, is available in the 
    WDK. You can also use the <a href="https://msdn.microsoft.com/191fcbd8-4542-4cad-955e-6951f3005fc5">LoadLibrary</a> and 
    <a href="https://msdn.microsoft.com/e425948c-5588-4a4f-994c-4e608af18439">GetProcAddress</a> functions to dynamically link to 
    Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>
 

 


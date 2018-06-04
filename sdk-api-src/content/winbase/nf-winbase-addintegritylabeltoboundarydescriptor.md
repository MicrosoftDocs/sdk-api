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

# AddIntegrityLabelToBoundaryDescriptor function


## -description


Adds a new required security identifier (SID) to the specified boundary descriptor.


## -parameters




### -param BoundaryDescriptor [in, out]

A handle to the boundary descriptor. The <a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a> function returns this handle.


### -param IntegrityLabel [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure that represents the mandatory integrity level for the namespace. Use one of the following RID values to create the SID:

<b>SECURITY_MANDATORY_UNTRUSTED_RID</b>
<b>SECURITY_MANDATORY_LOW_RID</b>
<b>SECURITY_MANDATORY_MEDIUM_RID</b>
<b>SECURITY_MANDATORY_SYSTEM_RID</b>
<b>SECURITY_MANDATORY_PROTECTED_PROCESS_RID</b>
For more information, see <a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">Well-Known SIDs</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A process can create a private namespace only with an integrity level that is  equal to or lower than the  current integrity level of the process. Therefore, a high integrity-level process can create a high, medium or low integrity-level namespace. A medium integrity-level process can create only a medium or low integrity-level namespace.

A process would usually specify a namespace at the same integrity level as the process for protection against squatting attacks by lower integrity-level processes. 

The security descriptor that the creator places on the namespace determines who can open the namespace. So a low or medium integrity-level process could be given permission to open a high integrity level namespace if the security descriptor of the namespace permits it.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0601 or later.




## -see-also




<a href="https://msdn.microsoft.com/c7789e90-8dfb-47ee-a0b2-906520982d84">CreateBoundaryDescriptor</a>
 

 


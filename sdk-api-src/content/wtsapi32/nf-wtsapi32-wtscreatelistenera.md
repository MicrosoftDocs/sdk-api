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

# WTSCreateListenerA function


## -description


Creates a new Remote Desktop Services listener or configures an existing listener.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Always set this  parameter to <b>WTS_CURRENT_SERVER_HANDLE</b>.


### -param pReserved [in]

This parameter is reserved. Always set this parameter to <b>NULL</b>.


### -param Reserved [in]

This parameter is reserved. Always set this parameter to zero.


### -param pListenerName [in]

A pointer to a null-terminated string that contains the name of the listener to create or configure.


### -param pBuffer [in]

A pointer to a <a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a> structure that contains configuration information for the listener.


### -param flag [in]

The purpose of the call. This parameter can be one of the following values.



#### WTS_LISTENER_CREATE (1 (0x1))

Create a new listener.



#### WTS_LISTENER_UPDATE (16 (0x10))

Update the settings of an existing listener.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



This function creates or configures a listener that uses   <a href="https://msdn.microsoft.com/442c3c7f-d04b-4dcd-945d-f6e0168c59d5">Remote Desktop Protocol</a> (RDP). Always set the <b>version</b> member of the <a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a> structure that is pointed to by the <i>pBuffer</i> parameter to one.

This function does not create or configure the security descriptor of the listener. When you call this function to create a new listener, the function assigns the default security descriptor to the new listener. To modify the security descriptor, call the <a href="https://msdn.microsoft.com/bc90d526-e252-4506-b781-66da5bd66ced">WTSSetListenerSecurity</a> function. For more information about security descriptors, see  <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>.

This function does not validate the settings for the new listener. Be sure that the settings are valid before calling this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a>



<a href="https://msdn.microsoft.com/bc90d526-e252-4506-b781-66da5bd66ced">WTSSetListenerSecurity</a>
 

 


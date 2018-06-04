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

# ACMDRIVERPROC callback function


## -description



The <b>acmDriverProc</b> function specifies a callback function used with the ACM driver. The <b>acmDriverProc</b> name is a placeholder for an application-defined function name. The actual name must be exported by including it in the module-definition file of the executable or DLL file.




## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4


### -param Arg5








#### - dwID

Identifier of the installable ACM driver.


#### - hdrvr

Handle to the installable ACM driver. This parameter is a unique handle the ACM assigns to the driver.


#### - lParam1

Message parameter.


#### - lParam2

Message parameter.


#### - uMsg

ACM driver message.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



Applications should not call any system-defined functions from inside a callback function, except for <b>PostMessage</b>, <a href="https://msdn.microsoft.com/57871ada-d2b7-48a9-bed0-3780b836c77a">timeGetSystemTime</a>, <a href="https://msdn.microsoft.com/f9d3a7a9-1457-4993-92f1-f888780a565e">timeGetTime</a>, <a href="https://msdn.microsoft.com/466fc196-a2bf-4fad-80bc-c18013d1c860">timeSetEvent</a>, <a href="https://msdn.microsoft.com/6b1d5163-359e-426f-9edc-3936accc57ee">timeKillEvent</a>, <a href="https://msdn.microsoft.com/b46d342a-7bfc-495a-98d3-e0c93ae4fd59">midiOutShortMsg</a>, <a href="https://msdn.microsoft.com/7fda802b-eed5-4a27-8bc0-1f43f4722d33">midiOutLongMsg</a>, and <b>OutputDebugStr</b>.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 


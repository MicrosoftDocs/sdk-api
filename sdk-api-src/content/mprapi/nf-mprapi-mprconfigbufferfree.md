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

# MprConfigBufferFree function


## -description


The 
<b>MprConfigBufferFree</b> function frees buffers allocated by calls to the following functions:

MprConfigXEnum
			

MprConfigXGetInfo
			

where X stands for Server, 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn895657">Interface</a>, Transport, or InterfaceTransport.


## -parameters




### -param pBuffer [in]

Pointer to a memory buffer allocated by a previous call to: 




MprConfigXEnum
						

MprConfigXGetInfo
						

where X stands for Server, 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn895657">Interface</a>, Transport, or InterfaceTransport.


## -returns



If the function succeeds, the return value is NO_ERROR.




## -see-also




<a href="https://msdn.microsoft.com/fce40bcc-df75-49cd-af02-5fea3a65aaac">MprConfigInterfaceEnum</a>



<a href="https://msdn.microsoft.com/f33f9e66-1668-4839-9c98-5945104110bc">MprConfigInterfaceGetInfo</a>



<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>



<a href="https://msdn.microsoft.com/2b0bb412-a480-43ff-b29a-cf4e7674d2c4">MprConfigInterfaceTransportGetInfo</a>



<a href="https://msdn.microsoft.com/6d3cd97a-96ef-4ecd-b2fd-2743ba79aa5b">MprConfigServerGetInfo</a>



<a href="https://msdn.microsoft.com/2abe30f4-564b-499f-a6d3-13da305a783c">MprConfigTransportEnum</a>



<a href="https://msdn.microsoft.com/84054313-f923-47d6-8019-c68a042d2d73">MprConfigTransportGetInfo</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 


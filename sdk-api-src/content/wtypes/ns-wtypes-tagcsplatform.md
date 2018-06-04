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

# tagCSPLATFORM structure


## -description


Contains an operating system platform and processor architecture.



## -struct-fields




### -field dwPlatformId

The operating system platform. See the <b>dwPlatformId</b> member of <a href="https://msdn.microsoft.com/a173df17-dad2-4330-aa66-4ff789fd7cc2">OSVERSIONINFO</a>.


### -field dwVersionHi

The major version of the operating system.


### -field dwVersionLo

The minor version of the operating system.


### -field dwProcessorArch

The processor architecture.
See the <b>wProcessorArchitecture</b> member of <a href="https://msdn.microsoft.com/971293b8-0af0-4bdf-a7d7-6b1bb80a469c">SYSTEM_INFO</a>.


## -see-also




<a href="https://msdn.microsoft.com/5d6a17e1-dcdd-4691-aec2-f63dbcb26027">QUERYCONTEXT</a>
 

 


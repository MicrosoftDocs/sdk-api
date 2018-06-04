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

# PrintError function


## -description


The 
<b>PrintError</b> function displays a system or application error message to the NetShell console.


## -parameters




### -param hModule [in]

A handle to the module from which the string should be loaded, or null for system error messages.


### -param dwErrId

TBD


### -param param

TBD




####### - ...

The arguments used to fill into the message.


#### - dwMsgId [in]

The identifier of the message to print.


## -returns



Returns the number of characters printed. Returns zero upon failure.




## -see-also




<a href="https://msdn.microsoft.com/6646a4f7-24b7-460c-8027-80485ac50785">PrintMessage</a>



<a href="https://msdn.microsoft.com/21f4688a-24fd-40b3-8da4-08c496b395f3">PrintMessageFromModule</a>
 

 


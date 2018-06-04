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

# PrintMessageFromModule function


## -description


The 
<b>PrintMessageFromModule</b> function displays localized output to the NetShell console.


## -parameters




### -param hModule [in]

A handle to the module from which the string should be loaded.


### -param dwMsgId [in]

The identifier  of the message to print.


### -param param

TBD




####### - ...

The arguments to fill into the message.


## -returns



Returns the number of characters printed. Returns zero upon failure.




## -remarks



Use this function when the format string, identified by the <i>dwMsgId</i> parameter, must be localized.




## -see-also




<a href="https://msdn.microsoft.com/de48b797-9cb5-4bc0-89d4-86dd7f56a610">PrintError</a>



<a href="https://msdn.microsoft.com/6646a4f7-24b7-460c-8027-80485ac50785">PrintMessage</a>
 

 


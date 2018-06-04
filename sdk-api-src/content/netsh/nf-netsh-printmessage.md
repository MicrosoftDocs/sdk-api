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

# PrintMessage function


## -description


The 
<b>PrintMessage</b> function displays output to the NetShell console.


## -parameters




### -param pwszFormat

TBD


### -param param

TBD




####### - ...


					The arguments used to fill into the message.


#### - rgwcInput [in]

A string to be output to the NetShell console.


## -returns



Returns the number of characters printed. Returns zero upon failure.




## -remarks



Use the 
<b>PrintMessage</b> function when the message to be output is not required to be localized.




## -see-also




<a href="https://msdn.microsoft.com/de48b797-9cb5-4bc0-89d4-86dd7f56a610">PrintError</a>



<a href="https://msdn.microsoft.com/21f4688a-24fd-40b3-8da4-08c496b395f3">PrintMessageFromModule</a>
 

 


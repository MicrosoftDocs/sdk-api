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

# CMSPAddress::GetDynamicTerminalClasses


## -description


The 
<b>GetDynamicTerminalClasses</b> method is called by our wrapper methods to get an array of dynamic terminal classes that can be used on this address. The semantics of the arguments are the same as for 
<a href="https://msdn.microsoft.com/8fffc00d-a783-47bc-a081-fe2116060da0">GetStaticTerminals</a>. This method simply asks the Terminal Manager for the terminal classes. MSPs that implement additional, custom types of dynamic terminals, or that want to disallow the use of certain dynamic terminal classes from the Terminal Manager, would want to override this method.


## -parameters




### -param pdwNumClasses [out]

Pointer to number of dynamic terminals.


### -param pTerminalClasses [out]

Pointer to array of 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interfaces.


## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 


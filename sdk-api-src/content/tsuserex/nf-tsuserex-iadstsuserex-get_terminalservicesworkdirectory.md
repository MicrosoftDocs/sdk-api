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

# IADsTSUserEx::get_TerminalServicesWorkDirectory


## -description


The working directory path for the user.

This property is read/write.


## -parameters


## -remarks



To set an initial application to start when the user logs on to the Remote Desktop Session Host (RD Session Host) server, you must first set the <a href="https://msdn.microsoft.com/43059f13-a1f1-44b2-96ac-2532656a0846">TerminalServicesInitialProgram</a> property, and then set this property.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/43059f13-a1f1-44b2-96ac-2532656a0846">TerminalServicesInitialProgram</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7af8fe94-15db-49dc-ba4a-b79601205f59">IADsTSUserEx</a>
 

 


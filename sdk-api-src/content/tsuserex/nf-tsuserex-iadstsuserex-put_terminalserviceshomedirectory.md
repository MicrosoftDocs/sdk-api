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

# IADsTSUserEx::put_TerminalServicesHomeDirectory


## -description


The root directory for the user. Each user on a Remote Desktop Session Host (RD Session Host) server has a unique root directory. This ensures that application information is stored separately for each user in a multiuser environment.

This property is read/write.


## -parameters


## -remarks



To set a root directory on the local computer, specify a local path; for example, C:\Path. To set a root directory in a network environment, you must first set the <a href="https://msdn.microsoft.com/e5cfa526-eff8-4a89-9b13-c4a06a416fe5">TerminalServicesHomeDrive</a> property, and then set this property to a UNC path.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e5cfa526-eff8-4a89-9b13-c4a06a416fe5">TerminalServicesHomeDrive</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7af8fe94-15db-49dc-ba4a-b79601205f59">IADsTSUserEx</a>
 

 


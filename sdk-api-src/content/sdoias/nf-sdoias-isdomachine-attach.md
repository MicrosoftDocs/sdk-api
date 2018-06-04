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

# ISdoMachine::Attach


## -description


The 
<b>Attach</b> method attaches to an SDO computer. Attaching to an SDO computer is the first step is using the SDO API to administer that computer.


## -parameters




### -param bstrComputerName [in]

Specifies a 
<a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> variable that contains the name of the computer to which to attach. If this parameter specifies a <b>NULL</b> string, the local computer is attached.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If a computer is already attached, the return value is <b>E_FAIL</b>.

The method may also return one of the following error codes.




## -remarks



Use the 
<a href="https://msdn.microsoft.com/ac2fe3e3-a1cb-4642-90af-2b0203e29251">ISdoMachine::GetAttachedComputer</a> method to determine if a computer is already attached.




## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/ac2fe3e3-a1cb-4642-90af-2b0203e29251">ISdoMachine::GetAttachedComputer</a>
 

 


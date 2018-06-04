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

# ISdoMachine::GetAttachedComputer


## -description


The <b>GetAttachedComputer</b> method 
    retrieves the name of the computer that is currently attached as an SDO computer.


## -parameters




### -param bstrComputerName [out]

Pointer to a <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> that 
      receives the name of the computer that is the currently-attached SDO computer.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If no computer is currently attached, the return value is <b>E_FAIL</b>.

The method may also return one of the following error codes.




## -remarks



The <b>GetAttachedComputer</b> allocates 
    the memory for the <a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> 
    variable. The calling application should free this memory by calling 
    <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.




## -see-also




<a href="https://msdn.microsoft.com/11372116-56eb-4d8e-8f28-4402835ee903">ISdoMachine</a>



<a href="https://msdn.microsoft.com/444ba670-8224-40bc-b0e4-585c682deafd">ISdoMachine::Attach</a>
 

 


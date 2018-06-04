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

# IGroupPolicyObject::OpenRemoteMachineGPO


## -description


The
    <b>OpenRemoteMachineGPO</b> method opens the default GPO for the specified remote computer and optionally loads the registry information.


## -parameters




### -param pszComputerName [in]

Specifies the name of the computer. The format of the name is \\<i>ComputerName</i>.


### -param dwFlags [in]

Specifies whether or not the registry information should be loaded for the GPO. This parameter can be one of the following values.



#### GPO_OPEN_LOAD_REGISTRY

Load the registry information.



#### GPO_OPEN_READ_ONLY

Open the GPO in read-only mode.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To retrieve the computer name of a remote GPO, you can call the 
<a href="https://msdn.microsoft.com/6ac20718-45d4-4a45-a95e-d159e4d6dacc">GetMachineName</a> method. Call 
<a href="https://msdn.microsoft.com/c986152b-59cd-4733-bcdd-ee7f0b6907ad">OpenLocalMachineGPO</a> to open the default GPO for a local computer.




## -see-also




<a href="https://msdn.microsoft.com/6ac20718-45d4-4a45-a95e-d159e4d6dacc">GetMachineName</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>



<a href="https://msdn.microsoft.com/c986152b-59cd-4733-bcdd-ee7f0b6907ad">OpenLocalMachineGPO</a>
 

 


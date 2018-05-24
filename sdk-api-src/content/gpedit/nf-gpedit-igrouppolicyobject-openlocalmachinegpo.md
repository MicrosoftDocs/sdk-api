---
UID: NF:gpedit.IGroupPolicyObject.OpenLocalMachineGPO
title: IGroupPolicyObject::OpenLocalMachineGPO
author: windows-driver-content
description: The OpenLocalMachineGPO method opens the default GPO for the computer and optionally loads the registry information.
old-location: policy\igrouppolicyobject_openlocalmachinegpo.htm
old-project: Policy
ms.assetid: c986152b-59cd-4733-bcdd-ee7f0b6907ad
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GPO_OPEN_LOAD_REGISTRY, GPO_OPEN_READ_ONLY, IGroupPolicyObject interface [Group Policy],OpenLocalMachineGPO method, IGroupPolicyObject.OpenLocalMachineGPO, IGroupPolicyObject::OpenLocalMachineGPO, OpenLocalMachineGPO, OpenLocalMachineGPO method [Group Policy], OpenLocalMachineGPO method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_openlocalmachinegpo, gpedit/IGroupPolicyObject::OpenLocalMachineGPO, policy.igrouppolicyobject_openlocalmachinegpo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IGroupPolicyObject.OpenLocalMachineGPO
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::OpenLocalMachineGPO


## -description


The
    <b>OpenLocalMachineGPO</b> method opens the default GPO for the computer and optionally loads the registry information.


## -parameters




### -param dwFlags [in]

Specifies whether or not the registry information should be loaded for the GPO. This parameter can be one of the following values.



#### GPO_OPEN_LOAD_REGISTRY

Load the registry information.



#### GPO_OPEN_READ_ONLY

Open the GPO in read-only mode.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To open the default GPO for a remote computer, you can call the 
<a href="https://msdn.microsoft.com/ac124b48-7eb6-473b-a96b-de9b1a903f28">OpenRemoteMachineGPO</a> method.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>



<a href="https://msdn.microsoft.com/ac124b48-7eb6-473b-a96b-de9b1a903f28">OpenRemoteMachineGPO</a>
 

 


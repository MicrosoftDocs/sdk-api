---
UID: NF:shobjidl_core.ICreatingProcess.OnCreating
title: ICreatingProcess::OnCreating
author: windows-sdk-content
description: Allows you to modify the parameters of the process being created.
old-location: shell\icreatingprocess_oncreating.htm
tech.root: shell
ms.assetid: 5A13ABDB-8453-41BE-AF0C-B5A07486CBE6
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ICreatingProcess interface [Windows Shell],OnCreating method, ICreatingProcess.OnCreating, ICreatingProcess::OnCreating, OnCreating, OnCreating method [Windows Shell], OnCreating method [Windows Shell],ICreatingProcess interface, shell.icreatingprocess_oncreating, shobjidl_core/ICreatingProcess::OnCreating
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ICreatingProcess.OnCreating
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreatingProcess::OnCreating


## -description


Allows you to modify the parameters of  the process being created.


## -parameters




### -param pcpi [in]

 A pointer to an <a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a> interface which allows you to set some parameters for the process that is being created.


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code, and the process is not created.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/68B89E8C-2868-4F33-87A5-66A2FEFC0441">ICreatingProcess</a>
 

 


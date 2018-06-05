---
UID: NF:shobjidl_core.ICreatingProcess.OnCreating
title: ICreatingProcess::OnCreating
author: windows-sdk-content
description: Allows you to modify the parameters of the process being created.
old-location: shell\icreatingprocess_oncreating.htm
old-project: shell
ms.assetid: 5A13ABDB-8453-41BE-AF0C-B5A07486CBE6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ICreatingProcess interface [Windows Shell],OnCreating method, ICreatingProcess.OnCreating, ICreatingProcess::OnCreating, OnCreating, OnCreating method [Windows Shell], OnCreating method [Windows Shell],ICreatingProcess interface, shell.icreatingprocess_oncreating, shobjidl_core/ICreatingProcess::OnCreating
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	ICreatingProcess.OnCreating
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/68B89E8C-2868-4F33-87A5-66A2FEFC0441">ICreatingProcess</a>
 

 


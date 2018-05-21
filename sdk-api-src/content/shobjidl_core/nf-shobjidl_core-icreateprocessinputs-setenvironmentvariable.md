---
UID: NF:shobjidl_core.ICreateProcessInputs.SetEnvironmentVariable
title: ICreateProcessInputs::SetEnvironmentVariable
author: windows-driver-content
description: Sets a variable in the environment of the created process.
old-location: shell\icreateprocessinputs_setenvironmentvariable.htm
old-project: shell
ms.assetid: 5898B21B-5D3B-4950-9DB4-5B7FD19C9187
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICreateProcessInputs interface [Windows Shell],SetEnvironmentVariable method, ICreateProcessInputs.SetEnvironmentVariable, ICreateProcessInputs::SetEnvironmentVariable, SetEnvironmentVariable, SetEnvironmentVariable method [Windows Shell], SetEnvironmentVariable method [Windows Shell],ICreateProcessInputs interface, shell.icreateprocessinputs_setenvironmentvariable, shobjidl_core/ICreateProcessInputs::SetEnvironmentVariable
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	ICreateProcessInputs.SetEnvironmentVariable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ICreateProcessInputs::SetEnvironmentVariable


## -description


Sets a variable in the environment of the created process.


## -parameters




### -param pszName [in]

 A null-terminated string specifying the name of a variable to be set in the environment of the process to be created. This parameter may not be <b>NULL</b>.


### -param pszValue [in]

 A null-terminated string specifying the value of the variable to be set in the environment of the process to be created. his parameter may not be <b>NULL</b>.


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -remarks



If a variable with the same name already exists in the environment of the created process, it is replaced.




## -see-also




<a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a>



<a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a>
 

 


---
UID: NF:shobjidl_core.ICreateProcessInputs.AddStartupFlags
title: ICreateProcessInputs::AddStartupFlags
author: windows-sdk-content
description: Additional flags that will be included in the STARTUPINFO structure passed to CreateProcess.
old-location: shell\icreateprocessinputs_addstartupflags.htm
tech.root: shell
ms.assetid: 62270ED9-678B-4D39-BFF1-3F9E10AAF03A
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: AddStartupFlags, AddStartupFlags method [Windows Shell], AddStartupFlags method [Windows Shell],ICreateProcessInputs interface, ICreateProcessInputs interface [Windows Shell],AddStartupFlags method, ICreateProcessInputs.AddStartupFlags, ICreateProcessInputs::AddStartupFlags, shell.icreateprocessinputs_addstartupflags, shobjidl_core/ICreateProcessInputs::AddStartupFlags
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
 - ICreateProcessInputs.AddStartupFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateProcessInputs::AddStartupFlags


## -description


 Additional flags that will be included in the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>.


## -parameters




### -param dwStartupInfoFlags [in]

 The flags that will be included in the <i>dwFlags</i> member of the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>. 


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -remarks



Any creation flags that were previously set will remain set. This method does not clear any creation flags.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a>



<a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>
 

 


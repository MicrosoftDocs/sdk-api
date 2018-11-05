---
UID: NF:shobjidl_core.ICreateProcessInputs.AddCreateFlags
title: ICreateProcessInputs::AddCreateFlags
author: windows-sdk-content
description: Set additional flags that will be included in the call to CreateProcess.
old-location: shell\icreateprocessinputs_addcreateflags.htm
tech.root: shell
ms.assetid: 07D9E07E-BDF8-46F7-AB75-A3041E96F1A1
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AddCreateFlags, AddCreateFlags method [Windows Shell], AddCreateFlags method [Windows Shell],ICreateProcessInputs interface, ICreateProcessInputs interface [Windows Shell],AddCreateFlags method, ICreateProcessInputs.AddCreateFlags, ICreateProcessInputs::AddCreateFlags, shell.icreateprocessinputs_addcreateflags, shobjidl_core/ICreateProcessInputs::AddCreateFlags
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
 - ICreateProcessInputs.AddCreateFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateProcessInputs::AddCreateFlags


## -description


 Set additional flags that will be included in the call to <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>.


## -parameters




### -param dwCreationFlags [in]

The flags that will be included in the <i>dwCreationFlags</i> parameter passed to <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>.


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -remarks



Any creation flags that were previously set will remain set. This method does not clear any creation flags.




## -see-also




<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a>



<a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a>



<a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a>



<a href="https://msdn.microsoft.com/B929D77A-FEE4-40A1-8B40-34E2E73048F9">SetCreateFlags</a>
 

 


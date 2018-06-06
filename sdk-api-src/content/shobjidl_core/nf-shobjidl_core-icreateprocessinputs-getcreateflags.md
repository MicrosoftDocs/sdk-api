---
UID: NF:shobjidl_core.ICreateProcessInputs.GetCreateFlags
title: ICreateProcessInputs::GetCreateFlags
author: windows-sdk-content
description: Gets the additional flags that will be passed to CreateProcess.
old-location: shell\icreateprocessinputs_getcreateflags.htm
old-project: shell
ms.assetid: 6884E7A0-17E8-4F5F-B0A4-85BD3745ED12
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCreateFlags, GetCreateFlags method [Windows Shell], GetCreateFlags method [Windows Shell],ICreateProcessInputs interface, ICreateProcessInputs interface [Windows Shell],GetCreateFlags method, ICreateProcessInputs.GetCreateFlags, ICreateProcessInputs::GetCreateFlags, shell.icreateprocessinputs_getcreateflags, shobjidl_core/ICreateProcessInputs::GetCreateFlags
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ICreateProcessInputs.GetCreateFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ICreateProcessInputs::GetCreateFlags


## -description


Gets the additional flags that will be passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.


## -parameters




### -param pdwCreationFlags [out]

 A pointer to a <b>DWORD</b> which receives the flags that will be passed as the <i>dwCreationFlags</i> parameter to <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>. 



## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/2C1756A3-FF40-4FBF-860D-06BB415DB695">ICreateProcessInputs</a>



<a href="https://msdn.microsoft.com/5A13ABDB-8453-41BE-AF0C-B5A07486CBE6">ICreatingProcess::OnCreating</a>
 

 


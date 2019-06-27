---
UID: NF:shobjidl_core.ICreateProcessInputs.AddStartupFlags
title: ICreateProcessInputs::AddStartupFlags (shobjidl_core.h)
author: windows-sdk-content
description: Additional flags that will be included in the STARTUPINFO structure passed to CreateProcess.
old-location: shell\icreateprocessinputs_addstartupflags.htm
tech.root: shell
ms.assetid: 62270ED9-678B-4D39-BFF1-3F9E10AAF03A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddStartupFlags, AddStartupFlags method [Windows Shell], AddStartupFlags method [Windows Shell],ICreateProcessInputs interface, ICreateProcessInputs interface [Windows Shell],AddStartupFlags method, ICreateProcessInputs.AddStartupFlags, ICreateProcessInputs::AddStartupFlags, shell.icreateprocessinputs_addstartupflags, shobjidl_core/ICreateProcessInputs::AddStartupFlags
ms.topic: method
f1_keywords: 
 - "shobjidl_core/ICreateProcessInputs.AddStartupFlags"
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
ms.custom: 19H1
---

# ICreateProcessInputs::AddStartupFlags


## -description


 Additional flags that will be included in the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-_startupinfoa">STARTUPINFO</a> structure passed to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.


## -parameters




### -param dwStartupInfoFlags [in]

 The flags that will be included in the <i>dwFlags</i> member of the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-_startupinfoa">STARTUPINFO</a> structure passed to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>. 


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -remarks



Any creation flags that were previously set will remain set. This method does not clear any creation flags.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-_startupinfoa">STARTUPINFO</a>
 

 


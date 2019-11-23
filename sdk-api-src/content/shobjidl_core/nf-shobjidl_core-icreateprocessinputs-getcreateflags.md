---
UID: NF:shobjidl_core.ICreateProcessInputs.GetCreateFlags
title: ICreateProcessInputs::GetCreateFlags (shobjidl_core.h)

description: Gets the additional flags that will be passed to CreateProcess.
old-location: shell\icreateprocessinputs_getcreateflags.htm
tech.root: shell
ms.assetid: 6884E7A0-17E8-4F5F-B0A4-85BD3745ED12

ms.date: 12/05/2018
ms.keywords: GetCreateFlags, GetCreateFlags method [Windows Shell], GetCreateFlags method [Windows Shell],ICreateProcessInputs interface, ICreateProcessInputs interface [Windows Shell],GetCreateFlags method, ICreateProcessInputs.GetCreateFlags, ICreateProcessInputs::GetCreateFlags, shell.icreateprocessinputs_getcreateflags, shobjidl_core/ICreateProcessInputs::GetCreateFlags
ms.topic: method
f1_keywords: 
 - "shobjidl_core/ICreateProcessInputs.GetCreateFlags"
dev_langs:
 - c++
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
 - ICreateProcessInputs.GetCreateFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateProcessInputs::GetCreateFlags


## -description


Gets the additional flags that will be passed to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.


## -parameters




### -param pdwCreationFlags [out]

 A pointer to a <b>DWORD</b> which receives the flags that will be passed as the <i>dwCreationFlags</i> parameter to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>. 



## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>
 

 


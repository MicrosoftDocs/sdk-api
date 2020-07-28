---
UID: NF:shobjidl_core.ICreateProcessInputs.SetHotKey
title: ICreateProcessInputs::SetHotKey (shobjidl_core.h)
description: Sets the hot key for the application.
helpviewer_keywords: ["ICreateProcessInputs interface [Windows Shell]","SetHotKey method","ICreateProcessInputs.SetHotKey","ICreateProcessInputs::SetHotKey","SetHotKey","SetHotKey method [Windows Shell]","SetHotKey method [Windows Shell]","ICreateProcessInputs interface","shell.icreateprocessinputs_sethotkey","shobjidl_core/ICreateProcessInputs::SetHotKey"]
old-location: shell\icreateprocessinputs_sethotkey.htm
tech.root: shell
ms.assetid: B54934CA-6345-4B06-BA5F-75FA4B5CEE4F
ms.date: 12/05/2018
ms.keywords: ICreateProcessInputs interface [Windows Shell],SetHotKey method, ICreateProcessInputs.SetHotKey, ICreateProcessInputs::SetHotKey, SetHotKey, SetHotKey method [Windows Shell], SetHotKey method [Windows Shell],ICreateProcessInputs interface, shell.icreateprocessinputs_sethotkey, shobjidl_core/ICreateProcessInputs::SetHotKey
f1_keywords:
- shobjidl_core/ICreateProcessInputs.SetHotKey
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
- ICreateProcessInputs.SetHotKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreateProcessInputs::SetHotKey


## -description


Sets the hot key for the application.


## -parameters




### -param wHotKey [in]

The hotkey to assign to the application. See the documentation of the <b>hStdIn</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure for more information.


## -returns



<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.




## -remarks



 This method also sets the <b>STARTF_USEHOTKEY</b> flag in the <b>dwFlags</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure passed to <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a>
 

 


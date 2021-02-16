---
UID: NF:shobjidl_core.ICreateProcessInputs.AddCreateFlags
title: ICreateProcessInputs::AddCreateFlags (shobjidl_core.h)
description: Set additional flags that will be included in the call to CreateProcess.
helpviewer_keywords: ["AddCreateFlags","AddCreateFlags method [Windows Shell]","AddCreateFlags method [Windows Shell]","ICreateProcessInputs interface","ICreateProcessInputs interface [Windows Shell]","AddCreateFlags method","ICreateProcessInputs.AddCreateFlags","ICreateProcessInputs::AddCreateFlags","shell.icreateprocessinputs_addcreateflags","shobjidl_core/ICreateProcessInputs::AddCreateFlags"]
old-location: shell\icreateprocessinputs_addcreateflags.htm
tech.root: shell
ms.assetid: 07D9E07E-BDF8-46F7-AB75-A3041E96F1A1
ms.date: 12/05/2018
ms.keywords: AddCreateFlags, AddCreateFlags method [Windows Shell], AddCreateFlags method [Windows Shell],ICreateProcessInputs interface, ICreateProcessInputs interface [Windows Shell],AddCreateFlags method, ICreateProcessInputs.AddCreateFlags, ICreateProcessInputs::AddCreateFlags, shell.icreateprocessinputs_addcreateflags, shobjidl_core/ICreateProcessInputs::AddCreateFlags
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICreateProcessInputs::AddCreateFlags
 - shobjidl_core/ICreateProcessInputs::AddCreateFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - ICreateProcessInputs.AddCreateFlags
---

# ICreateProcessInputs::AddCreateFlags


## -description

 Set additional flags that will be included in the call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

## -parameters

### -param dwCreationFlags [in]

The flags that will be included in the <i>dwCreationFlags</i> parameter passed to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

## -returns

<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.

## -remarks

Any creation flags that were previously set will remain set. This method does not clear any creation flags.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>



<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-setcreateflags">SetCreateFlags</a>
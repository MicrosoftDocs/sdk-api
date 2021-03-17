---
UID: NF:shobjidl_core.ICreateProcessInputs.SetCreateFlags
title: ICreateProcessInputs::SetCreateFlags (shobjidl_core.h)
description: Set the flags that will be included in the call to CreateProcess.
helpviewer_keywords: ["ICreateProcessInputs interface [Windows Shell]","SetCreateFlags method","ICreateProcessInputs.SetCreateFlags","ICreateProcessInputs::SetCreateFlags","SetCreateFlags","SetCreateFlags method [Windows Shell]","SetCreateFlags method [Windows Shell]","ICreateProcessInputs interface","shell.icreateprocessinputs_setcreateflags","shobjidl_core/ICreateProcessInputs::SetCreateFlags"]
old-location: shell\icreateprocessinputs_setcreateflags.htm
tech.root: shell
ms.assetid: B929D77A-FEE4-40A1-8B40-34E2E73048F9
ms.date: 12/05/2018
ms.keywords: ICreateProcessInputs interface [Windows Shell],SetCreateFlags method, ICreateProcessInputs.SetCreateFlags, ICreateProcessInputs::SetCreateFlags, SetCreateFlags, SetCreateFlags method [Windows Shell], SetCreateFlags method [Windows Shell],ICreateProcessInputs interface, shell.icreateprocessinputs_setcreateflags, shobjidl_core/ICreateProcessInputs::SetCreateFlags
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
 - ICreateProcessInputs::SetCreateFlags
 - shobjidl_core/ICreateProcessInputs::SetCreateFlags
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
 - ICreateProcessInputs.SetCreateFlags
---

# ICreateProcessInputs::SetCreateFlags


## -description

 Set the flags that will be included in the call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

## -parameters

### -param dwCreationFlags [in]

The flags that will be passed to the <i>dwCreationFlags</i> parameter to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

## -returns

<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.

## -remarks

 Any flags set by a previous call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-addcreateflags">AddCreateFlags</a> or <b>SetCreateFlags </b> will be replaced by the values specified by <i>dwCreationFlags</i>. Use <b>AddCreateFlags</b> to set flags without clearing  flags that are already set.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreateprocessinputs-addcreateflags">AddCreateFlags</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>



<a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a>
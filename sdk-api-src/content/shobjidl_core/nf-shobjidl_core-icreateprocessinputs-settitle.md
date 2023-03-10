---
UID: NF:shobjidl_core.ICreateProcessInputs.SetTitle
title: ICreateProcessInputs::SetTitle (shobjidl_core.h)
description: Sets the title that will be passed CreateProcess.
helpviewer_keywords: ["ICreateProcessInputs interface [Windows Shell]","SetTitle method","ICreateProcessInputs.SetTitle","ICreateProcessInputs::SetTitle","SetTitle","SetTitle method [Windows Shell]","SetTitle method [Windows Shell]","ICreateProcessInputs interface","shell.icreateprocessinputs_settitle","shobjidl_core/ICreateProcessInputs::SetTitle"]
old-location: shell\icreateprocessinputs_settitle.htm
tech.root: shell
ms.assetid: BFCDC5B1-740E-4CE9-8E06-75F3ECA7B7E6
ms.date: 12/05/2018
ms.keywords: ICreateProcessInputs interface [Windows Shell],SetTitle method, ICreateProcessInputs.SetTitle, ICreateProcessInputs::SetTitle, SetTitle, SetTitle method [Windows Shell], SetTitle method [Windows Shell],ICreateProcessInputs interface, shell.icreateprocessinputs_settitle, shobjidl_core/ICreateProcessInputs::SetTitle
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
 - ICreateProcessInputs::SetTitle
 - shobjidl_core/ICreateProcessInputs::SetTitle
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
 - ICreateProcessInputs.SetTitle
---

# ICreateProcessInputs::SetTitle


## -description

 Sets the title that will be passed <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.

## -parameters

### -param pszTitle [in]

 A null-terminated string specifying the title that will be passed in the <b>lpTitle</b> member of the <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure passed to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>. This parameter may not be <b>NULL</b>.

## -returns

<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>
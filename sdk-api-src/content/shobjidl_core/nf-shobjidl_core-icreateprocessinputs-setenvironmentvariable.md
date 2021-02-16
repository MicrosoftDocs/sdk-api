---
UID: NF:shobjidl_core.ICreateProcessInputs.SetEnvironmentVariable
title: ICreateProcessInputs::SetEnvironmentVariable (shobjidl_core.h)
description: Sets a variable in the environment of the created process.
helpviewer_keywords: ["ICreateProcessInputs interface [Windows Shell]","SetEnvironmentVariable method","ICreateProcessInputs.SetEnvironmentVariable","ICreateProcessInputs::SetEnvironmentVariable","SetEnvironmentVariable","SetEnvironmentVariable method [Windows Shell]","SetEnvironmentVariable method [Windows Shell]","ICreateProcessInputs interface","shell.icreateprocessinputs_setenvironmentvariable","shobjidl_core/ICreateProcessInputs::SetEnvironmentVariable"]
old-location: shell\icreateprocessinputs_setenvironmentvariable.htm
tech.root: shell
ms.assetid: 5898B21B-5D3B-4950-9DB4-5B7FD19C9187
ms.date: 12/05/2018
ms.keywords: ICreateProcessInputs interface [Windows Shell],SetEnvironmentVariable method, ICreateProcessInputs.SetEnvironmentVariable, ICreateProcessInputs::SetEnvironmentVariable, SetEnvironmentVariable, SetEnvironmentVariable method [Windows Shell], SetEnvironmentVariable method [Windows Shell],ICreateProcessInputs interface, shell.icreateprocessinputs_setenvironmentvariable, shobjidl_core/ICreateProcessInputs::SetEnvironmentVariable
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
 - ICreateProcessInputs::SetEnvironmentVariable
 - shobjidl_core/ICreateProcessInputs::SetEnvironmentVariable
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
 - ICreateProcessInputs.SetEnvironmentVariable
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

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>
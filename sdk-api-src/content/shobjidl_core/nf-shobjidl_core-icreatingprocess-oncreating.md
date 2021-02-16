---
UID: NF:shobjidl_core.ICreatingProcess.OnCreating
title: ICreatingProcess::OnCreating (shobjidl_core.h)
description: Allows you to modify the parameters of the process being created.
helpviewer_keywords: ["ICreatingProcess interface [Windows Shell]","OnCreating method","ICreatingProcess.OnCreating","ICreatingProcess::OnCreating","OnCreating","OnCreating method [Windows Shell]","OnCreating method [Windows Shell]","ICreatingProcess interface","shell.icreatingprocess_oncreating","shobjidl_core/ICreatingProcess::OnCreating"]
old-location: shell\icreatingprocess_oncreating.htm
tech.root: shell
ms.assetid: 5A13ABDB-8453-41BE-AF0C-B5A07486CBE6
ms.date: 12/05/2018
ms.keywords: ICreatingProcess interface [Windows Shell],OnCreating method, ICreatingProcess.OnCreating, ICreatingProcess::OnCreating, OnCreating, OnCreating method [Windows Shell], OnCreating method [Windows Shell],ICreatingProcess interface, shell.icreatingprocess_oncreating, shobjidl_core/ICreatingProcess::OnCreating
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
 - ICreatingProcess::OnCreating
 - shobjidl_core/ICreatingProcess::OnCreating
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
 - ICreatingProcess.OnCreating
---

# ICreatingProcess::OnCreating


## -description

Allows you to modify the parameters of  the process being created.

## -parameters

### -param pcpi [in]

 A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs">ICreateProcessInputs</a> interface which allows you to set some parameters for the process that is being created.

## -returns

<b> S_OK</b> if the method succeeds. Otherwise, an <b>HRESULT</b> error code, and the process is not created.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess">ICreatingProcess</a>
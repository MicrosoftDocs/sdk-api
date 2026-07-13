---
UID: NN:shobjidl_core.ICreateProcessInputs
title: ICreateProcessInputs (shobjidl_core.h)
description: Used by the ICreatingProcess interface to alter some parameters of the process that is being created.
helpviewer_keywords: ["ICreateProcessInputs","ICreateProcessInputs interface [Windows Shell]","ICreateProcessInputs interface [Windows Shell]","described","shell.icreateprocessinputs","shobjidl_core/ICreateProcessInputs"]
old-location: shell\icreateprocessinputs.htm
tech.root: shell
ms.assetid: 2C1756A3-FF40-4FBF-860D-06BB415DB695
ms.date: 12/05/2018
ms.keywords: ICreateProcessInputs, ICreateProcessInputs interface [Windows Shell], ICreateProcessInputs interface [Windows Shell],described, shell.icreateprocessinputs, shobjidl_core/ICreateProcessInputs
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
 - ICreateProcessInputs
 - shobjidl_core/ICreateProcessInputs
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
 - ICreateProcessInputs
---

# ICreateProcessInputs interface


## -description

Used by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess">ICreatingProcess</a> interface to alter some parameters of the process that is being created.

## -inheritance

The <b>ICreateProcessInputs</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateProcessInputs</b> also has these types of members:

## -remarks

Applications do not implement this interface.

A pointer to this interface is passed to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icreatingprocess-oncreating">ICreatingProcess::OnCreating</a>.

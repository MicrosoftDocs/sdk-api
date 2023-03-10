---
UID: NF:shobjidl_core.IAssocHandlerInvoker.Invoke
title: IAssocHandlerInvoker::Invoke (shobjidl_core.h)
description: Invokes an associated application handler.
helpviewer_keywords: ["IAssocHandlerInvoker interface [Windows Shell]","Invoke method","IAssocHandlerInvoker.Invoke","IAssocHandlerInvoker::Invoke","Invoke","Invoke method [Windows Shell]","Invoke method [Windows Shell]","IAssocHandlerInvoker interface","_shell_IAssocHandlerInvoker_Invoke","shell.IAssocHandlerInvoker_Invoke","shobjidl_core/IAssocHandlerInvoker::Invoke"]
old-location: shell\IAssocHandlerInvoker_Invoke.htm
tech.root: shell
ms.assetid: 9b5de945-b177-4cbc-817c-447b2174323e
ms.date: 12/05/2018
ms.keywords: IAssocHandlerInvoker interface [Windows Shell],Invoke method, IAssocHandlerInvoker.Invoke, IAssocHandlerInvoker::Invoke, Invoke, Invoke method [Windows Shell], Invoke method [Windows Shell],IAssocHandlerInvoker interface, _shell_IAssocHandlerInvoker_Invoke, shell.IAssocHandlerInvoker_Invoke, shobjidl_core/IAssocHandlerInvoker::Invoke
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
 - IAssocHandlerInvoker::Invoke
 - shobjidl_core/IAssocHandlerInvoker::Invoke
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
 - IAssocHandlerInvoker.Invoke
---

# IAssocHandlerInvoker::Invoke


## -description

Invokes an associated application handler.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There is no guarantee that a given association handler will support a particular selection, especially if multiple items are selected.  Before attempting to invoke the selection via this method, it is recommended to call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iassochandlerinvoker-supportsselection">IAssocHandlerInvoker::SupportsSelection</a>.

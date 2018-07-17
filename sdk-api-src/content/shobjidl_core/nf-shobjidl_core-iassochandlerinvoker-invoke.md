---
UID: NF:shobjidl_core.IAssocHandlerInvoker.Invoke
title: IAssocHandlerInvoker::Invoke
author: windows-sdk-content
description: Invokes an associated application handler.
old-location: shell\IAssocHandlerInvoker_Invoke.htm
old-project: shell
ms.assetid: 9b5de945-b177-4cbc-817c-447b2174323e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IAssocHandlerInvoker interface [Windows Shell],Invoke method, IAssocHandlerInvoker.Invoke, IAssocHandlerInvoker::Invoke, Invoke, Invoke method [Windows Shell], Invoke method [Windows Shell],IAssocHandlerInvoker interface, _shell_IAssocHandlerInvoker_Invoke, shell.IAssocHandlerInvoker_Invoke, shobjidl_core/IAssocHandlerInvoker::Invoke
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAssocHandlerInvoker.Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAssocHandlerInvoker::Invoke


## -description


Invokes an associated application handler.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There is no guarantee that a given association handler will support a particular selection, especially if multiple items are selected.  Before attempting to invoke the selection via this method, it is recommended to call <a href="https://msdn.microsoft.com/a4000557-2a89-494c-8b0e-c67a2e2c4445">IAssocHandlerInvoker::SupportsSelection</a>.
		




---
UID: NF:shobjidl_core.IAssocHandlerInvoker.SupportsSelection
title: IAssocHandlerInvoker::SupportsSelection
author: windows-sdk-content
description: Determines whether an invoker supports its selection.
old-location: shell\IAssocHandlerInvoker_SupportsSelection.htm
tech.root: shell
ms.assetid: a4000557-2a89-494c-8b0e-c67a2e2c4445
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IAssocHandlerInvoker interface [Windows Shell],SupportsSelection method, IAssocHandlerInvoker.SupportsSelection, IAssocHandlerInvoker::SupportsSelection, SupportsSelection, SupportsSelection method [Windows Shell], SupportsSelection method [Windows Shell],IAssocHandlerInvoker interface, _shell_IAssocHandlerInvoker_SupportsSelection, shell.IAssocHandlerInvoker_SupportsSelection, shobjidl_core/IAssocHandlerInvoker::SupportsSelection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAssocHandlerInvoker.SupportsSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAssocHandlerInvoker::SupportsSelection


## -description


Determines whether an invoker supports its selection.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if this instance supports its selection, or <b>S_FALSE</b> otherwise.




## -remarks



For example, this method should return whether an application (as selected from an "Open With" context menu) can <b>Open</b> a file.
             




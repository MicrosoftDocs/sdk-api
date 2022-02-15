---
UID: NN:shobjidl_core.ITransferSource
title: ITransferSource (shobjidl_core.h)
description: Exposes methods to manipulate IShellItem, including copy, move, recycle, and others. This interface is offered to provide more control over file operations by providing an ITransferSource::Advise method.
helpviewer_keywords: ["ITransferSource","ITransferSource interface [Windows Shell]","ITransferSource interface [Windows Shell]","described","_shell_ITransferSource","shell.ITransferSource","shobjidl_core/ITransferSource"]
old-location: shell\ITransferSource.htm
tech.root: shell
ms.assetid: 341966d4-f9cf-457d-97ef-8e6107544283
ms.date: 12/05/2018
ms.keywords: ITransferSource, ITransferSource interface [Windows Shell], ITransferSource interface [Windows Shell],described, _shell_ITransferSource, shell.ITransferSource, shobjidl_core/ITransferSource
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
 - ITransferSource
 - shobjidl_core/ITransferSource
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
 - ITransferSource
---

# ITransferSource interface


## -description

 Exposes methods to manipulate <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>, including copy, move, recycle, and others. This interface is offered to provide more control over file operations by providing an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise">ITransferSource::Advise</a> method.

## -inheritance

The <b>ITransferSource</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransferSource</b> also has these types of members:


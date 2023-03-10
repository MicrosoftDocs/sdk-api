---
UID: NN:shobjidl_core.ITransferDestination
title: ITransferDestination (shobjidl_core.h)
description: Exposes methods that create a destination Shell item for a copy or move operation. This interface is provided to allow more control over file operations by providing an ITransferDestination::Advise method.
helpviewer_keywords: ["ITransferDestination","ITransferDestination interface [Windows Shell]","ITransferDestination interface [Windows Shell]","described","_shell_ITransferDestination","shell.ITransferDestination","shobjidl_core/ITransferDestination"]
old-location: shell\ITransferDestination.htm
tech.root: shell
ms.assetid: 8d0049e0-e227-40ae-a282-cdc17f227e24
ms.date: 12/05/2018
ms.keywords: ITransferDestination, ITransferDestination interface [Windows Shell], ITransferDestination interface [Windows Shell],described, _shell_ITransferDestination, shell.ITransferDestination, shobjidl_core/ITransferDestination
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
 - ITransferDestination
 - shobjidl_core/ITransferDestination
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
 - ITransferDestination
---

# ITransferDestination interface


## -description

Exposes methods that create a destination Shell item for a copy or move operation. This interface is provided to allow more control over file operations by providing an <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise">ITransferDestination::Advise</a> method.

## -inheritance

The <b>ITransferDestination</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransferDestination</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a>

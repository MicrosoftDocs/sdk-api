---
UID: NN:shobjidl_core.ITransferMediumItem
title: ITransferMediumItem (shobjidl_core.h)
author: windows-sdk-content
description: Used by a copy engine to get the item on which to call QueryInterface to return a pointer to interface ITransferDestination or interface ITransferSource. These interfaces can be queried and enumerated for copy, move, or delete operations.
old-location: shell\ITransferMediumItem.htm
tech.root: shell
ms.assetid: 28b4397c-dcb1-4c81-b6a3-d6abd7f7ad24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITransferMediumItem, ITransferMediumItem interface [Windows Shell], ITransferMediumItem interface [Windows Shell],described, _shell_ITransferMediumItem, shell.ITransferMediumItem, shobjidl_core/ITransferMediumItem
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
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
 - ITransferMediumItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransferMediumItem interface


## -description


Used by a copy engine to get the item on which to call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> to return a pointer to interface <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination">ITransferDestination</a> or interface <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource">ITransferSource</a>. These interfaces can be queried and enumerated for copy, move, or delete operations.


## -remarks



This interface provides only the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem">IRelatedItem</a> interface, from which it inherits.




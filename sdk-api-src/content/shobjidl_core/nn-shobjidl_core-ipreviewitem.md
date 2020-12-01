---
UID: NN:shobjidl_core.IPreviewItem
title: IPreviewItem (shobjidl_core.h)
description: Identifies an item that will be shown in the preview pane.
helpviewer_keywords: ["IPreviewItem","IPreviewItem interface [Windows Shell]","IPreviewItem interface [Windows Shell]","described","_shell_IPreviewItem","shell.IPreviewItem","shobjidl_core/IPreviewItem"]
old-location: shell\IPreviewItem.htm
tech.root: shell
ms.assetid: ad228cc9-2c13-4e28-8468-7f8c66eb221e
ms.date: 12/05/2018
ms.keywords: IPreviewItem, IPreviewItem interface [Windows Shell], IPreviewItem interface [Windows Shell],described, _shell_IPreviewItem, shell.IPreviewItem, shobjidl_core/IPreviewItem
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IPreviewItem
 - shobjidl_core/IPreviewItem
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
 - IPreviewItem
---

# IPreviewItem interface


## -description

Identifies an item that will be shown in the preview pane.

## -remarks

This interface provides only the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem">IRelatedItem</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface for system-provided data objects is provided with Windows. Custom data sources that want to expose this information must implement the interface as part of their data object.
---
UID: NN:shobjidl_core.IDisplayItem
title: IDisplayItem (shobjidl_core.h)
description: Exposes methods that find a version of the current item to be used to get display properties, such as the item name, that will be displayed in the UI.
helpviewer_keywords: ["IDisplayItem","IDisplayItem interface [Windows Shell]","IDisplayItem interface [Windows Shell]","described","_shell_IDisplayItem","shell.IDisplayItem","shobjidl_core/IDisplayItem"]
old-location: shell\IDisplayItem.htm
tech.root: shell
ms.assetid: 78e06db0-9440-4578-bc17-96444946432a
ms.date: 12/05/2018
ms.keywords: IDisplayItem, IDisplayItem interface [Windows Shell], IDisplayItem interface [Windows Shell],described, _shell_IDisplayItem, shell.IDisplayItem, shobjidl_core/IDisplayItem
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDisplayItem
 - shobjidl_core/IDisplayItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDisplayItem
---

# IDisplayItem interface


## -description

Exposes methods that find a version of the current item to be used to get display properties, such as the item name, that will be displayed in the UI. Used by the copy engine dialogs to provide the UI with an appropriate item to display. If no other version can be found, the current item is used.

## -remarks

This interface provides only the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem">IRelatedItem</a> interface, from which it inherits.
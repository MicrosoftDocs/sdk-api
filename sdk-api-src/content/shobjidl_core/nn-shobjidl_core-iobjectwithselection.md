---
UID: NN:shobjidl_core.IObjectWithSelection
title: IObjectWithSelection (shobjidl_core.h)
description: Exposes methods that get or set selected items represented by a Shell item array.
helpviewer_keywords: ["IObjectWithSelection","IObjectWithSelection interface [Windows Shell]","IObjectWithSelection interface [Windows Shell]","described","_shell_IObjectWithSelection","shell.IObjectWithSelection","shobjidl_core/IObjectWithSelection"]
old-location: shell\IObjectWithSelection.htm
tech.root: shell
ms.assetid: 8fb248eb-73e7-4db0-8585-4accafe332d0
ms.date: 12/05/2018
ms.keywords: IObjectWithSelection, IObjectWithSelection interface [Windows Shell], IObjectWithSelection interface [Windows Shell],described, _shell_IObjectWithSelection, shell.IObjectWithSelection, shobjidl_core/IObjectWithSelection
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IObjectWithSelection
 - shobjidl_core/IObjectWithSelection
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
 - IObjectWithSelection
---

# IObjectWithSelection interface


## -description

Exposes methods that get or set selected items represented by a Shell item array.

## -inheritance

The <b>IObjectWithSelection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectWithSelection</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented by verbs that implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand">IExecuteCommand</a>. This allows objects to invoke the verb on the selection through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexecutecommand-execute">IExecuteCommand::Execute</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
<b>IObjectWithSelection</b> is used by Windows Explorer to invoke a verb on the selected items. Do not call this interface directly.

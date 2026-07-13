---
UID: NN:shobjidl_core.IFileDialogEvents
title: IFileDialogEvents (shobjidl_core.h)
description: Exposes methods that allow notification of events within a common file dialog.
helpviewer_keywords: ["IFileDialogEvents","IFileDialogEvents interface [Windows Shell]","IFileDialogEvents interface [Windows Shell]","described","shell.IFileDialogEvents","shell_IFileDialogEvents","shobjidl_core/IFileDialogEvents"]
old-location: shell\IFileDialogEvents.htm
tech.root: shell
ms.assetid: c55107a3-ae0a-4b46-80a3-8a731b47976c
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents, IFileDialogEvents interface [Windows Shell], IFileDialogEvents interface [Windows Shell],described, shell.IFileDialogEvents, shell_IFileDialogEvents, shobjidl_core/IFileDialogEvents
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
 - IFileDialogEvents
 - shobjidl_core/IFileDialogEvents
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
 - IFileDialogEvents
---

# IFileDialogEvents interface


## -description

Exposes methods that allow notification of events within a common file dialog.

## -inheritance

The <b>IFileDialogEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileDialogEvents</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileDialogEvents</b> is implemented by an application that is a client of the common file dialog browser. Methods that are not implemented should return E_NOTIMPL. An example of <b>IFileDialogEvents</b> can be found in the <a href="/previous-versions/windows/desktop/legacy/dd940349(v=vs.85)">Common File Dialog</a> SDK sample.

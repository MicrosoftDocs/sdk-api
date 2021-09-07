---
UID: NN:shobjidl_core.IActionProgressDialog
title: IActionProgressDialog (shobjidl_core.h)
description: Exposes methods that initialize and stop a progress dialog.
helpviewer_keywords: ["IActionProgressDialog","IActionProgressDialog interface [Windows Shell]","IActionProgressDialog interface [Windows Shell]","described","_shell_IActionProgressDialog","shell.IActionProgressDialog","shobjidl_core/IActionProgressDialog"]
old-location: shell\IActionProgressDialog.htm
tech.root: shell
ms.assetid: f3c0e4ae-f93f-4ee2-873a-d9370044e922
ms.date: 12/05/2018
ms.keywords: IActionProgressDialog, IActionProgressDialog interface [Windows Shell], IActionProgressDialog interface [Windows Shell],described, _shell_IActionProgressDialog, shell.IActionProgressDialog, shobjidl_core/IActionProgressDialog
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Browseui.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActionProgressDialog
 - shobjidl_core/IActionProgressDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Browseui.dll
api_name:
 - IActionProgressDialog
---

# IActionProgressDialog interface


## -description

Exposes methods that initialize and stop a progress dialog.

## -inheritance

The <b>IActionProgressDialog</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActionProgressDialog</b> also has these types of members:

## -remarks

To instantiate an object that implements this interface, call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> using the class identifier (CLSID) CLSID_ProgressDialog.

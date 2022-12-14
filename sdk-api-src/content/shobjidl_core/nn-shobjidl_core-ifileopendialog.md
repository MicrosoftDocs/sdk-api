---
UID: NN:shobjidl_core.IFileOpenDialog
title: IFileOpenDialog (shobjidl_core.h)
description: Extends the IFileDialog interface by adding methods specific to the open dialog.
helpviewer_keywords: ["IFileOpenDialog","IFileOpenDialog interface [Windows Shell]","IFileOpenDialog interface [Windows Shell]","described","shell.IFileOpenDialog","shell_IFileOpenDialog","shobjidl_core/IFileOpenDialog"]
old-location: shell\IFileOpenDialog.htm
tech.root: shell
ms.assetid: f95b7106-18ab-4f7f-8d3f-267ac0293245
ms.date: 12/05/2018
ms.keywords: IFileOpenDialog, IFileOpenDialog interface [Windows Shell], IFileOpenDialog interface [Windows Shell],described, shell.IFileOpenDialog, shell_IFileOpenDialog, shobjidl_core/IFileOpenDialog
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileOpenDialog
 - shobjidl_core/IFileOpenDialog
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
 - IFileOpenDialog
---

# IFileOpenDialog interface


## -description

Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface by adding methods specific to the open dialog.

## -inheritance

The <b>IFileOpenDialog</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>. <b>IFileOpenDialog</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileOpenDialog</b> is implemented by the common file open dialog (CLSID_FileOpenDialog).

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface, from which it inherits.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesavedialog">IFileSaveDialog</a>

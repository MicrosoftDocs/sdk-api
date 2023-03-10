---
UID: NN:shobjidl_core.IFileSaveDialog
title: IFileSaveDialog (shobjidl_core.h)
description: Extends the IFileDialog interface by adding methods specific to the save dialog, which include those that provide support for the collection of metadata to be persisted with the file.
helpviewer_keywords: ["IFileSaveDialog","IFileSaveDialog interface [Windows Shell]","IFileSaveDialog interface [Windows Shell]","described","shell.IFileSaveDialog","shell_IFileSaveDialog","shobjidl_core/IFileSaveDialog"]
old-location: shell\IFileSaveDialog.htm
tech.root: shell
ms.assetid: 74021f92-54ff-4c02-a8cf-49bcd7b9171e
ms.date: 12/05/2018
ms.keywords: IFileSaveDialog, IFileSaveDialog interface [Windows Shell], IFileSaveDialog interface [Windows Shell],described, shell.IFileSaveDialog, shell_IFileSaveDialog, shobjidl_core/IFileSaveDialog
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
 - IFileSaveDialog
 - shobjidl_core/IFileSaveDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog
---

# IFileSaveDialog interface


## -description

Extends the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface by adding methods specific to the save dialog, which include those that provide support for the collection of metadata to be persisted with the file.

## -inheritance

The <b>IFileSaveDialog</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>. <b>IFileSaveDialog</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileSaveDialog</b> is implemented by the common file save dialog (CLSID_FileSaveDialog).

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface, from which it inherits.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog">IFileOpenDialog</a>

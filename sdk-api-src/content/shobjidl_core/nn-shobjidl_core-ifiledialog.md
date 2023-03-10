---
UID: NN:shobjidl_core.IFileDialog
title: IFileDialog (shobjidl_core.h)
description: Exposes methods that initialize, show, and get results from the common file dialog.
helpviewer_keywords: ["IFileDialog","IFileDialog interface [Windows Shell]","IFileDialog interface [Windows Shell]","described","shell.IFileDialog","shell_IFileDialog","shobjidl_core/IFileDialog"]
old-location: shell\IFileDialog.htm
tech.root: shell
ms.assetid: 9341bb68-2410-4e03-8acd-fef29287b61c
ms.date: 12/05/2018
ms.keywords: IFileDialog, IFileDialog interface [Windows Shell], IFileDialog interface [Windows Shell],described, shell.IFileDialog, shell_IFileDialog, shobjidl_core/IFileDialog
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - IFileDialog
 - shobjidl_core/IFileDialog
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
 - IFileDialog
---

# IFileDialog interface


## -description

Exposes methods that initialize, show, and get results from the common file dialog.

## -inheritance

The <b>IFileDialog</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow">IModalWindow</a>. <b>IFileDialog</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileDialog</b> is implemented by the common file open dialog (CLSID_FileOpenDialog) and
file save dialog (CLSID_FileSaveDialog).

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog">IFileOpenDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesavedialog">IFileSaveDialog</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow">IModalWindow</a>

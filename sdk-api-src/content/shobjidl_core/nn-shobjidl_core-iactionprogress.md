---
UID: NN:shobjidl_core.IActionProgress
title: IActionProgress (shobjidl_core.h)
description: Represents the abstract base class from which progress-driven operations can inherit.
helpviewer_keywords: ["IActionProgress","IActionProgress interface [Windows Shell]","IActionProgress interface [Windows Shell]","described","shell.IActionProgress","shell_IActionProgress","shobjidl_core/IActionProgress"]
old-location: shell\IActionProgress.htm
tech.root: shell
ms.assetid: e742e381-0fd2-482a-81a0-7b43d11b073b
ms.date: 12/05/2018
ms.keywords: IActionProgress, IActionProgress interface [Windows Shell], IActionProgress interface [Windows Shell],described, shell.IActionProgress, shell_IActionProgress, shobjidl_core/IActionProgress
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActionProgress
 - shobjidl_core/IActionProgress
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
 - IActionProgress
---

# IActionProgress interface


## -description

Represents the abstract base class from which progress-driven operations can inherit.

## -inheritance

The <b>IActionProgress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActionProgress</b> also has these types of members:

## -remarks

This class is an abstract class that may not be instantiated. It provides a framework that derived classes can use to implement a progress callback. This callback can be used by applications to report progress of actions to the UI. Here, "Actions" refers to operations that may take a significant amount of time, such as downloading or copying files, and during which a visible progress indication would be appropriate.

Applications typically do not implement this interface. Much of the functionality that users interact with during actions is provided by the CProgressDialog class (CLSID_ProgressDialog) that implements <b>IActionProgress</b> and displays progress in a dialog box. If a solution requiring a mechanism other than a dialog box is required, <b>IActionProgress</b> can be used to provide basic progress indicator functionality.

Once implemented, classes should call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin">IActionProgress::Begin</a> when an action is started. Periodically, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-updateprogress">IActionProgress::UpdateProgress</a> should be called to update the UI with progress information, and detailed textual information should be conveyed to the UI by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-updatetext">IActionProgress::UpdateText</a>. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-querycancel">IActionProgress::QueryCancel</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-resetcancel">IActionProgress::ResetCancel</a> should be called to handle cancellation requests. Once the operation ends, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-end">IActionProgress::End</a> should be called.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>

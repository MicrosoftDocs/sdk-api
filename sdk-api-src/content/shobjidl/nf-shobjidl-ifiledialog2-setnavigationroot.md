---
UID: NF:shobjidl.IFileDialog2.SetNavigationRoot
title: IFileDialog2::SetNavigationRoot (shobjidl.h)
description: Specifies a top-level location from which to begin browsing a namespace, for instance in the Save dialog's Browse folder option. Users cannot navigate above this location.
helpviewer_keywords: ["IFileDialog2 interface [Windows Shell]","SetNavigationRoot method","IFileDialog2.SetNavigationRoot","IFileDialog2::SetNavigationRoot","SetNavigationRoot","SetNavigationRoot method [Windows Shell]","SetNavigationRoot method [Windows Shell]","IFileDialog2 interface","_shell_IFileDialog2_SetNavigationRoot","shell.IFileDialog2_SetNavigationRoot","shobjidl/IFileDialog2::SetNavigationRoot"]
old-location: shell\IFileDialog2_SetNavigationRoot.htm
tech.root: shell
ms.assetid: 2ca6b5e7-5867-40f7-a949-e76815407005
ms.date: 12/05/2018
ms.keywords: IFileDialog2 interface [Windows Shell],SetNavigationRoot method, IFileDialog2.SetNavigationRoot, IFileDialog2::SetNavigationRoot, SetNavigationRoot, SetNavigationRoot method [Windows Shell], SetNavigationRoot method [Windows Shell],IFileDialog2 interface, _shell_IFileDialog2_SetNavigationRoot, shell.IFileDialog2_SetNavigationRoot, shobjidl/IFileDialog2::SetNavigationRoot
req.header: shobjidl.h
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
req.lib: Comdlg32.lib
req.dll: Comdlg32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileDialog2::SetNavigationRoot
 - shobjidl/IFileDialog2::SetNavigationRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IFileDialog2.SetNavigationRoot
---

# IFileDialog2::SetNavigationRoot


## -description

Specifies a top-level location from which to begin browsing a namespace, for instance in the <b>Save</b> dialog's <b>Browse folder</b> option. Users cannot navigate above this location.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a></b>

Pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the navigation root.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>SetNavigationRoot</b> can be used by applications that want to restrict navigation to a certain area of the Shell namespace. Items in the navigation pane are replaced with the supplied item, to guide the user from navigating outside of this part of the namespace.

This method cannot be called while the dialog is being displayed.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-ifiledialog2">IFileDialog2</a>
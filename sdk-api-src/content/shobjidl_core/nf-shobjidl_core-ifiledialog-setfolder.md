---
UID: NF:shobjidl_core.IFileDialog.SetFolder
title: IFileDialog::SetFolder (shobjidl_core.h)
description: Sets a folder that is always selected when the dialog is opened, regardless of previous user action.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetFolder method","IFileDialog.SetFolder","IFileDialog::SetFolder","SetFolder","SetFolder method [Windows Shell]","SetFolder method [Windows Shell]","IFileDialog interface","shell.IFileDialog_SetFolder","shell_IFileDialog_SetFolder","shobjidl_core/IFileDialog::SetFolder"]
old-location: shell\IFileDialog_SetFolder.htm
tech.root: shell
ms.assetid: 3f300c70-cae8-43bb-95d4-25ac4be9b4c4
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFolder method, IFileDialog.SetFolder, IFileDialog::SetFolder, SetFolder, SetFolder method [Windows Shell], SetFolder method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetFolder, shell_IFileDialog_SetFolder, shobjidl_core/IFileDialog::SetFolder
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
 - IFileDialog::SetFolder
 - shobjidl_core/IFileDialog::SetFolder
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
 - IFileDialog.SetFolder
---

# IFileDialog::SetFolder


## -description

Sets a folder that is always selected when the dialog is opened, regardless of previous user action.

## -parameters

### -param psi [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the interface that represents the folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This folder overrides any "most recently used" folder. If this method is called while the dialog is displayed, it causes the dialog to navigate to the specified folder.

In general, we do not recommended the use of this method. If you call <b>SetFolder</b> before you display the dialog box, the most recent location that the user saved to or opened from is not shown. Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should therefore be avoided. In almost all instances, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder">IFileDialog::SetDefaultFolder</a> is the better method.

As of Windows 7, if the path of the folder specified through <i>psi</i> is the default path of a <a href="/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)">known folder</a>, the known folder's current path is used in the dialog. That path might not be the same as the path specified in <i>psi</i>; for instance, if the known folder has been redirected. If the known folder is a library (virtual folders Documents, Music, Pictures, and Videos), the library's path is used in the dialog. If the specified library is hidden (as they are by default as of Windows 8.1), the library's default save location is used in the dialog, such as the Microsoft OneDrive Documents folder for the Documents library. Because of these mappings, the folder location used in the dialog might not be exactly as you specified when you called this method.
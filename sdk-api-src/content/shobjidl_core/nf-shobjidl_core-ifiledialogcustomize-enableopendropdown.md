---
UID: NF:shobjidl_core.IFileDialogCustomize.EnableOpenDropDown
title: IFileDialogCustomize::EnableOpenDropDown (shobjidl_core.h)
description: Enables a drop-down list on the Open or Save button in the dialog.
helpviewer_keywords: ["EnableOpenDropDown","EnableOpenDropDown method [Windows Shell]","EnableOpenDropDown method [Windows Shell]","IFileDialogCustomize interface","IFileDialogCustomize interface [Windows Shell]","EnableOpenDropDown method","IFileDialogCustomize.EnableOpenDropDown","IFileDialogCustomize::EnableOpenDropDown","shell.IFileDialogCustomize_EnableOpenDropDown","shell_IFileDialogCustomize_EnableOpenDropDown","shobjidl_core/IFileDialogCustomize::EnableOpenDropDown"]
old-location: shell\IFileDialogCustomize_EnableOpenDropDown.htm
tech.root: shell
ms.assetid: b4626030-0fc7-4329-b897-01f4ce8728a0
ms.date: 12/05/2018
ms.keywords: EnableOpenDropDown, EnableOpenDropDown method [Windows Shell], EnableOpenDropDown method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],EnableOpenDropDown method, IFileDialogCustomize.EnableOpenDropDown, IFileDialogCustomize::EnableOpenDropDown, shell.IFileDialogCustomize_EnableOpenDropDown, shell_IFileDialogCustomize_EnableOpenDropDown, shobjidl_core/IFileDialogCustomize::EnableOpenDropDown
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
 - IFileDialogCustomize::EnableOpenDropDown
 - shobjidl_core/IFileDialogCustomize::EnableOpenDropDown
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
 - IFileDialogCustomize.EnableOpenDropDown
---

# IFileDialogCustomize::EnableOpenDropDown


## -description

Enables a drop-down list on the <b>Open</b> or <b>Save</b> button in the dialog.

## -parameters

### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the drop-down list.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Open or Save button label takes on the text of the first item in the drop-down. This overrides any label set by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setokbuttonlabel">IFileDialog::SetOkButtonLabel</a>.

 Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogcustomize-addcontrolitem">IFileDialogCustomize::AddControlItem</a> to add items to the drop-down.
---
UID: NF:shobjidl_core.IFileDialog.SetFilter
title: IFileDialog::SetFilter (shobjidl_core.h)
description: SetFilter is no longer available for use as of Windows 7.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetFilter method","IFileDialog.SetFilter","IFileDialog::SetFilter","SetFilter","SetFilter method [Windows Shell]","SetFilter method [Windows Shell]","IFileDialog interface","_shell_IFileDialog_SetFilter","shell.IFileDialog_SetFilter","shobjidl_core/IFileDialog::SetFilter"]
old-location: shell\IFileDialog_SetFilter.htm
tech.root: shell
ms.assetid: 6f650ae2-77c4-496c-8b8b-279c69eaaf65
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFilter method, IFileDialog.SetFilter, IFileDialog::SetFilter, SetFilter, SetFilter method [Windows Shell], SetFilter method [Windows Shell],IFileDialog interface, _shell_IFileDialog_SetFilter, shell.IFileDialog_SetFilter, shobjidl_core/IFileDialog::SetFilter
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
 - IFileDialog::SetFilter
 - shobjidl_core/IFileDialog::SetFilter
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
 - IFileDialog.SetFilter
---

# IFileDialog::SetFilter


## -description

<p class="CCE_Message">[Deprecated. <b>SetFilter</b> is no longer available for use as of Windows 7.]

Sets the filter.

## -parameters

### -param pFilter

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter">IShellItemFilter</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter">IShellItemFilter</a> that is to be set.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be used if the application needs to perform special filtering to remove some items from the dialog box's view.  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemfilter-includeitem">IncludeItem</a> will be called for each item that would normally be included in the view. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemfilter-getenumflagsforitem">GetEnumFlagsForItem</a> is not used.
To filter by file type, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes">IFileDialog::SetFileTypes</a> should be used, because in folders with a large number of items it may offer better performance than applying an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter">IShellItemFilter</a>.
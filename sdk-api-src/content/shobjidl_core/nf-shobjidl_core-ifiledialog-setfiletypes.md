---
UID: NF:shobjidl_core.IFileDialog.SetFileTypes
title: IFileDialog::SetFileTypes (shobjidl_core.h)
description: Sets the file types that the dialog can open or save.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetFileTypes method","IFileDialog.SetFileTypes","IFileDialog::SetFileTypes","SetFileTypes","SetFileTypes method [Windows Shell]","SetFileTypes method [Windows Shell]","IFileDialog interface","shell.IFileDialog_SetFileTypes","shell_IFileDialog_SetFileTypes","shobjidl_core/IFileDialog::SetFileTypes"]
old-location: shell\IFileDialog_SetFileTypes.htm
tech.root: shell
ms.assetid: ca850988-7f2f-4faf-9ded-14db476fc452
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFileTypes method, IFileDialog.SetFileTypes, IFileDialog::SetFileTypes, SetFileTypes, SetFileTypes method [Windows Shell], SetFileTypes method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetFileTypes, shell_IFileDialog_SetFileTypes, shobjidl_core/IFileDialog::SetFileTypes
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
 - IFileDialog::SetFileTypes
 - shobjidl_core/IFileDialog::SetFileTypes
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
 - IFileDialog.SetFileTypes
---

# IFileDialog::SetFileTypes


## -description

Sets the file types that the dialog can open or save.

## -parameters

### -param cFileTypes [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>rgFilterSpec</i>.

### -param rgFilterSpec [in]

Type: <b>const <a href="/windows/desktop/api/shtypes/ns-shtypes-comdlg_filterspec">COMDLG_FILTERSPEC</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/shtypes/ns-shtypes-comdlg_filterspec">COMDLG_FILTERSPEC</a> structures, each representing a file type.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes">SetFileTypes</a> has already been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <b>FOS_PICKFOLDERS</b> flag was set in the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions">IFileDialog::SetOptions</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>rgFilterSpec</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

When using the <b>Open</b> dialog, the file types declared there are used to filter the view. When using the <b>Save</b> dialog, these values determine which file name extension is appended to the file name.

This method must be called before the dialog is shown and can only be called once for each dialog instance. File types cannot be modified once the Common Item dialog box is displayed.


#### Examples

The following code example demonstrates the use of the array of <a href="/windows/desktop/api/shtypes/ns-shtypes-comdlg_filterspec">COMDLG_FILTERSPEC</a> structures in the context of this method. The example array consists of three <b>COMDLG_FILTERSPEC</b> structures. The first declares two patterns for the dialog filter, the second declares a single pattern, and the last shows files of all types. The variables szJPG, szBMP, and szAll are assumed to be previously declared strings that provide a friendly name for each filter.


```cpp
COMDLG_FILTERSPEC rgSpec[] =
{ 
    { szJPG, L"*.jpg;*.jpeg" },
    { szBMP, L"*.bmp" },
    { szAll, L"*.*" },
};
```
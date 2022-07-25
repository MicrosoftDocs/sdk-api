---
UID: NF:shobjidl_core.IShellLibrary.GetIcon
title: IShellLibrary::GetIcon (shobjidl_core.h)
description: Gets the default icon for the library.
helpviewer_keywords: ["GetIcon","GetIcon method [Windows Shell]","GetIcon method [Windows Shell]","IShellLibrary interface","IShellLibrary interface [Windows Shell]","GetIcon method","IShellLibrary.GetIcon","IShellLibrary::GetIcon","_shell_IShellLibrary_GetIcon","shell.IShellLibrary_GetIcon","shobjidl_core/IShellLibrary::GetIcon"]
old-location: shell\IShellLibrary_GetIcon.htm
tech.root: shell
ms.assetid: e39bd663-3f2d-4b72-9882-1313ee457844
ms.date: 12/05/2018
ms.keywords: GetIcon, GetIcon method [Windows Shell], GetIcon method [Windows Shell],IShellLibrary interface, IShellLibrary interface [Windows Shell],GetIcon method, IShellLibrary.GetIcon, IShellLibrary::GetIcon, _shell_IShellLibrary_GetIcon, shell.IShellLibrary_GetIcon, shobjidl_core/IShellLibrary::GetIcon
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLibrary::GetIcon
 - shobjidl_core/IShellLibrary::GetIcon
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
 - IShellLibrary.GetIcon
---

# IShellLibrary::GetIcon


## -description

Gets the default icon for the library.

## -parameters

### -param ppszIcon [out]

Type: <b>LPWSTR*</b>

A null-terminated Unicode string that describes the location of the default icon. The  string is returned as <code>ModuleFileName,ResourceIndex</code> or <code>ModuleFileName,-ResourceID</code>. 

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>ModuleFileName</td>
<td>The file name of the module file that contains the icon resource.</td>
</tr>
<tr>
<td>ResourceIndex</td>
<td>If the number that follows the comma is positive, the index of the resource in the module file.</td>
</tr>
<tr>
<td>-ResourceID</td>
<td>If the number that follows the comma is negative, the absolute value of the number is the resource ID of the icon in the module file.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For additional information on parsing the string returned in <i>ppszIcon</i>, see <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa">PathParseIconLocation</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/shell/library-schema-entry">Library Description Schema</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa">PathParseIconLocation</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>
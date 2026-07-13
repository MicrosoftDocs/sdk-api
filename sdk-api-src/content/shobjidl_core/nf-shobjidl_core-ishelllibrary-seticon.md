---
UID: NF:shobjidl_core.IShellLibrary.SetIcon
title: IShellLibrary::SetIcon (shobjidl_core.h)
description: Sets the default icon for the library.
helpviewer_keywords: ["IShellLibrary interface [Windows Shell]","SetIcon method","IShellLibrary.SetIcon","IShellLibrary::SetIcon","SetIcon","SetIcon method [Windows Shell]","SetIcon method [Windows Shell]","IShellLibrary interface","_shell_IShellLibrary_SetIcon","shell.IShellLibrary_SetIcon","shobjidl_core/IShellLibrary::SetIcon"]
old-location: shell\IShellLibrary_SetIcon.htm
tech.root: shell
ms.assetid: 7d6d6bd5-14cc-432b-b712-64bac78f5df9
ms.date: 12/05/2018
ms.keywords: IShellLibrary interface [Windows Shell],SetIcon method, IShellLibrary.SetIcon, IShellLibrary::SetIcon, SetIcon, SetIcon method [Windows Shell], SetIcon method [Windows Shell],IShellLibrary interface, _shell_IShellLibrary_SetIcon, shell.IShellLibrary_SetIcon, shobjidl_core/IShellLibrary::SetIcon
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
 - IShellLibrary::SetIcon
 - shobjidl_core/IShellLibrary::SetIcon
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
 - IShellLibrary.SetIcon
---

# IShellLibrary::SetIcon


## -description

Sets the default icon for the library.

## -parameters

### -param pszIcon [in]

Type: <b>LPCWSTR</b>

A null-terminated Unicode string that describes the location of the default icon. The string must be formatted as <code>ModuleFileName,ResourceIndex</code> or <code>ModuleFileName,-ResourceID</code>. 

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
<td>A positive decimal number that specifies the index of the icon resource in the module file.</td>
</tr>
<tr>
<td>-ResourceID</td>
<td>A negative decimal number whose absolute value is the resource ID of the icon resource in the module file.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information on the format of the <i>pszIcon</i> parameter, see <a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa">PathParseIconLocation</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa">PathParseIconLocation</a>



<a href="/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)">Windows Libraries</a>
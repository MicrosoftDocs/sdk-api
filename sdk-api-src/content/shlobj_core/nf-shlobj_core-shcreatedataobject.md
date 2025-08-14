---
UID: NF:shlobj_core.SHCreateDataObject
title: SHCreateDataObject function (shlobj_core.h)
description: Creates a data object in a parent folder.
helpviewer_keywords: ["SHCreateDataObject","SHCreateDataObject function [Windows Shell]","_shell_SHCreateDataObject","shell.SHCreateDataObject","shlobj_core/SHCreateDataObject"]
old-location: shell\SHCreateDataObject.htm
tech.root: shell
ms.assetid: d56cdafe-9463-43a5-8ef0-6cfaf0c524a8
ms.date: 12/05/2018
ms.keywords: SHCreateDataObject, SHCreateDataObject function [Windows Shell], _shell_SHCreateDataObject, shell.SHCreateDataObject, shlobj_core/SHCreateDataObject
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateDataObject
 - shlobj_core/SHCreateDataObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-dataobject-l1-1-1.dll
 - Shell32.dll
 - windows.storage.dll
 - API-MS-Win-Shell-Dataobject-L1-1-0.dll
api_name:
 - SHCreateDataObject
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# SHCreateDataObject function


## -description

Creates a data object in a parent folder.

## -parameters

### -param pidlFolder [in, optional]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> (PIDL) of the parent folder that contains the data object.

### -param cidl [in]

Type: <b>UINT</b>

The number of file objects or subfolders specified in the <i>apidl</i> parameter.

### -param apidl [in, optional]

Type: <b>PCUITEMID_CHILD_ARRAY</b>

An array of pointers to constant <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structures, each of which uniquely identifies a file object or subfolder relative to the parent folder. Each item identifier list must contain exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure followed by a terminating zero.

### -param pdtInner [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to interface <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>. This parameter can be <b>NULL</b>. Specify <i>pdtInner</i> only if the data object created needs to support additional <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>  clipboard formats beyond the default formats it is assigned at creation.  Alternatively, provide support for populating the created data object using non-default clipboard formats by calling method <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a> and specifying the format in the <b>FORMATETC</b> structure passed in parameter <i>pFormatetc</i>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>. This must be IID_IDataObject.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface pointer requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is typically called when implementing method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">IShellFolder::GetUIObjectOf</a>. When an interface pointer of interface ID  IID_IDataObject is requested (using parameter <i>riid</i>), the implementer can return the interface pointer on the object created with <b>SHCreateDataObject</b> in response.

This function supports the <a href="/windows/desktop/shell/clipboard">CFSTR_SHELLIDLIST</a> (also known as HIDA) clipboard format and also has generic support for arbitrary clipboard formats through <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>. For more information on clipboard formats, see Shell Clipboard Formats.

The new data object is intended to be used in operations such as drag-and-drop, in which the data is stored in the clipboard with a given format.

We recommend that you use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cidldata_createfromidarray">CIDLData_CreateFromIDArray</a>

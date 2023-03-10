---
UID: NF:shobjidl_core.IShellFolder.EnumObjects
title: IShellFolder::EnumObjects (shobjidl_core.h)
description: Enables a client to determine the contents of a folder by creating an item identifier enumeration object and returning its IEnumIDList interface. The methods supported by that interface can then be used to enumerate the folder's contents.
helpviewer_keywords: ["EnumObjects","EnumObjects method [Windows Shell]","EnumObjects method [Windows Shell]","IShellFolder interface","EnumObjects method [Windows Shell]","IShellFolder2 interface","IShellFolder interface [Windows Shell]","EnumObjects method","IShellFolder.EnumObjects","IShellFolder2 interface [Windows Shell]","EnumObjects method","IShellFolder2::EnumObjects","IShellFolder::EnumObjects","_win32_IShellFolder_EnumObjects","shell.IShellFolder_EnumObjects","shobjidl_core/IShellFolder2::EnumObjects","shobjidl_core/IShellFolder::EnumObjects"]
old-location: shell\IShellFolder_EnumObjects.htm
tech.root: shell
ms.assetid: 248bec8b-0bf4-47d5-adb3-31a685a2c359
ms.date: 12/05/2018
ms.keywords: EnumObjects, EnumObjects method [Windows Shell], EnumObjects method [Windows Shell],IShellFolder interface, EnumObjects method [Windows Shell],IShellFolder2 interface, IShellFolder interface [Windows Shell],EnumObjects method, IShellFolder.EnumObjects, IShellFolder2 interface [Windows Shell],EnumObjects method, IShellFolder2::EnumObjects, IShellFolder::EnumObjects, _win32_IShellFolder_EnumObjects, shell.IShellFolder_EnumObjects, shobjidl_core/IShellFolder2::EnumObjects, shobjidl_core/IShellFolder::EnumObjects
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder::EnumObjects
 - shobjidl_core/IShellFolder::EnumObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolder.EnumObjects
 - IShellFolder2.EnumObjects
---

# IShellFolder::EnumObjects


## -description

Enables a client to determine the contents of a folder by creating an item identifier enumeration object and returning its <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a> interface. The methods supported by that interface can then be used to enumerate the folder's contents.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

If user input is required to perform the enumeration, this window handle should be used by the enumeration object as the parent window to take user input. An example would be a dialog box to ask for a password or prompt the user to insert a CD or floppy disk. If <i>hwndOwner</i> is set to <b>NULL</b>, the enumerator should not post any messages, and if user input is required, it should silently fail.

### -param grfFlags [in]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a></b>

Flags indicating which items to include in the enumeration. For a list of possible values, see the <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf">SHCONTF</a> enumerated type.

### -param ppenumIDList [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>**</b>

The address that receives a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a> interface of the enumeration object created by this method. If an error occurs or no suitable subobjects are found, <i>ppenumIDList</i> is set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns <code>S_OK</code> if successful, or an error value otherwise. Some implementations may also return <code>S_FALSE</code>, indicating that there are no children matching the <i>grfFlags</i> that were passed in. If <code>S_FALSE</code> is returned, <i>ppenumIDList</i> is set to <code>NULL</code>.

## -remarks

If the method returns S_OK, then <i>ppenumIDList</i> receives a pointer to an enumerator. In this case, the calling application must free the returned <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a> object by calling its <b>Release</b> method.

If the method returns S_FALSE, then the folder contains no suitable subobjects and the pointer specified in <i>ppenumIDList</i> is set to <b>NULL</b>.

If the method fails, an error value is returned and the pointer specified in <i>ppenumIDList</i> is set to <b>NULL</b>.

If the folder contains no suitable subobjects, then the <b>IShellFolder::EnumObjects</b> method is permitted either to set *<i>ppenumIDList</i> to <b>NULL</b> and return S_FALSE, or to set *<i>ppenumIDList</i> to an enumerator that produces no objects and return S_OK. Calling applications must be prepared for both success cases.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder">SHGetDesktopFolder</a>
---
UID: NF:shlobj_core.IACList.Expand
title: IACList::Expand (shlobj_core.h)
description: Requests that the autocompletion client generate candidate strings associated with a specified item in its namespace.
helpviewer_keywords: ["Expand","Expand method [Windows Shell]","Expand method [Windows Shell]","IACList interface","IACList interface [Windows Shell]","Expand method","IACList.Expand","IACList::Expand","_win32_IACList_Expand","shell.IACList_Expand","shlobj_core/IACList::Expand"]
old-location: shell\IACList_Expand.htm
tech.root: shell
ms.assetid: 0d4ff090-dac7-4918-bea9-312be1d960e6
ms.date: 12/05/2018
ms.keywords: Expand, Expand method [Windows Shell], Expand method [Windows Shell],IACList interface, IACList interface [Windows Shell],Expand method, IACList.Expand, IACList::Expand, _win32_IACList_Expand, shell.IACList_Expand, shlobj_core/IACList::Expand
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IACList::Expand
 - shlobj_core/IACList::Expand
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
 - IACList.Expand
---

# IACList::Expand


## -description

Requests that the autocompletion client generate candidate strings associated with a specified item in its namespace.

## -parameters

### -param pszExpand [in]

Type: <b>PCWSTR</b>

A pointer to a null-terminated, Unicode string to be expanded by the autocomplete object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The autocomplete object calls this method when a delimiter is entered in the edit control. If the string pointed to by <i>pszExpand</i> matches an item in the autocompletion client's namespace, the client generates strings for those items that fall immediately under <i>pszExpand</i> in its namespace hierarchy. The client returns those strings next time the autocompletion object calls the client's <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface.

For example, assuming that the client's namespace consists of all the files and folders on the C: drive, and <i>pszExpand</i> is set to "C:\Program Files\", the client should generate a list of strings corresponding to the fully qualified paths of the files and subfolders of "C:\Program Files\".

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist">IACList</a>
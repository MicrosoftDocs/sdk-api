---
UID: NF:shlwapi.IQueryAssociations.Init
title: IQueryAssociations::Init (shlwapi.h)
description: Initializes the IQueryAssociations interface and sets the root key to the appropriate ProgID.
helpviewer_keywords: ["CLSID","Executable name","File name extension","IQueryAssociations interface [Windows Shell]","Init method","IQueryAssociations.Init","IQueryAssociations::Init","Init","Init method [Windows Shell]","Init method [Windows Shell]","IQueryAssociations interface","ProgID","_win32_IQueryAssociations_Init","shell.IQueryAssociations_Init","shlwapi/IQueryAssociations::Init"]
old-location: shell\IQueryAssociations_Init.htm
tech.root: shell
ms.assetid: cb1bcfc1-dbaa-48f8-8547-408f6560753e
ms.date: 12/05/2018
ms.keywords: CLSID, Executable name, File name extension, IQueryAssociations interface [Windows Shell],Init method, IQueryAssociations.Init, IQueryAssociations::Init, Init, Init method [Windows Shell], Init method [Windows Shell],IQueryAssociations interface, ProgID, _win32_IQueryAssociations_Init, shell.IQueryAssociations_Init, shlwapi/IQueryAssociations::Init
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Shlwapi.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IQueryAssociations::Init
 - shlwapi/IQueryAssociations::Init
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
 - IQueryAssociations.Init
---

# IQueryAssociations::Init


## -description

Initializes the <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface and sets the root key to the appropriate ProgID.

## -parameters

### -param flags [in]

Type: <b><a href="/windows/win32/shell/assocf_str">ASSOCF</a></b>

A flag that specifies how the search is to be initialized. It is typically set to zero, but it can also take one of the following <a href="/windows/win32/shell/assocf_str">ASSOCF</a> values. 
					
                    

<ul>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_INIT_BYEXENAME</a>
</li>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_INIT_DEFAULTTOFOLDER</a>
</li>
<li>
<a href="/windows/win32/shell/assocf_str">ASSOCF_INIT_DEFAULTTOSTAR</a>
</li>
</ul>

### -param pszAssoc [in, optional]

Type: <b>LPCWSTR</b>

A Unicode string that is used to determine the root key. If a value is specified for <i>hkProgid</i>, set this parameter to <b>NULL</b>. Four types of string can be used:



#### File name extension

A file name extension, such as .txt.



#### CLSID

A CLSID GUID in the standard "{GUID}" format.



#### ProgID

An application's ProgID, such as <b>Word.Document.8</b>.



#### Executable name

The name of an application's .exe file. The <a href="/windows/win32/shell/assocf_str">ASSOCF_OPEN_BYEXENAME</a> flag must be set in <i>flags</i>.

### -param hkProgid [in, optional]

Type: <b>HKEY</b>

The HKEY value of the subkey that is used as a root key. The search looks only below this key. If a value is specified for <i>pwszAssoc</i>, set this parameter to <b>NULL</b>.

### -param hwnd [in, optional]

Type: <b>HWND</b>

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method initializes the interface, and is also called each time you need to specify a new root key. You can use <i>pwszAssoc</i> to specify a string, such as a file name extension or its associated ProgID, that identifies the root key. You can also specify the root key's HKEY value. <b>Init</b> will then use this information to locate the root key in the registry. Subsequent calls to the other <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> methods will use it as their starting point and search for the information in the root key's subkeys.

## -see-also

<a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a>
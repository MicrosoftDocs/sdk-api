---
UID: NF:shobjidl_core.SHCreateItemFromParsingName
title: SHCreateItemFromParsingName function (shobjidl_core.h)
description: Creates and initializes a Shell item object from a parsing name.
helpviewer_keywords: ["SHCreateItemFromParsingName","SHCreateItemFromParsingName function [Windows Shell]","_shell_SHCreateItemFromParsingName","shell.SHCreateItemFromParsingName","shobjidl_core/SHCreateItemFromParsingName"]
old-location: shell\SHCreateItemFromParsingName.htm
tech.root: shell
ms.assetid: 81e48318-b6a4-4b1a-8b78-21c00b9dc485
ms.date: 12/05/2018
ms.keywords: SHCreateItemFromParsingName, SHCreateItemFromParsingName function [Windows Shell], _shell_SHCreateItemFromParsingName, shell.SHCreateItemFromParsingName, shobjidl_core/SHCreateItemFromParsingName
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - SHCreateItemFromParsingName
 - shobjidl_core/SHCreateItemFromParsingName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - api-ms-win-shell-namespace-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Ext-MS-Win-shell-shell32-L1-2-0.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - Windows.Storage.Dll
api_name:
 - SHCreateItemFromParsingName
---

# SHCreateItemFromParsingName function


## -description

Creates and initializes a Shell item object from a parsing name.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a display name.

### -param pbc [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

Optional. A pointer to a bind context used to pass parameters as inputs and outputs to the parsing function. These passed parameters are often specific to the data source and are documented by the data source owners. For example, the file system data source accepts the name being parsed (as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure), using the <a href="/windows/desktop/shell/str-constants">STR_FILE_SYS_BIND_DATA</a> bind context parameter.


<a href="/windows/desktop/shell/str-constants">STR_PARSE_PREFER_FOLDER_BROWSING</a> can be passed to indicate that URLs are parsed using the file system data source when possible. Construct a bind context object using <a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> and populate the values using <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam">IBindCtx::RegisterObjectParam</a>. See <b>Bind Context String Keys</b> for a complete list of these. See the <a href="/previous-versions/windows/desktop/legacy/dd940368(v=vs.85)">Parsing With Parameters Sample</a> for an example of the use of this parameter.



If no data is being passed to or received from the parsing function, this value can be <b>NULL</b>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically <b>IID_IShellItem</b> or <b>IID_IShellItem2</b>.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2">IShellItem2</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct <b>IID</b> based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.
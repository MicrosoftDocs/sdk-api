---
UID: NF:shobjidl_core.SHCreateItemFromParsingName
title: SHCreateItemFromParsingName function
author: windows-sdk-content
description: Creates and initializes a Shell item object from a parsing name.
old-location: shell\SHCreateItemFromParsingName.htm
tech.root: shell
ms.assetid: 81e48318-b6a4-4b1a-8b78-21c00b9dc485
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: SHCreateItemFromParsingName, SHCreateItemFromParsingName function [Windows Shell], _shell_SHCreateItemFromParsingName, shell.SHCreateItemFromParsingName, shobjidl_core/SHCreateItemFromParsingName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - API-MS-Win-Shell-Namespace-L1-1-0.dll
 - Ext-MS-Win-shell-shell32-L1-2-0.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
 - Windows.Storage.Dll
api_name:
 - SHCreateItemFromParsingName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHCreateItemFromParsingName function


## -description


Creates and initializes a Shell item object from a parsing name.


## -parameters




### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a display name.


### -param pbc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e4c8abb5-0c89-44dd-8d95-efbfcc999b46">IBindCtx</a>*</b>

Optional. A pointer to a bind context used to pass parameters as inputs and outputs to the parsing function. These passed parameters are often specific to the data source and are documented by the data source owners. For example, the file system data source accepts the name being parsed (as a <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure), using the <a href="https://msdn.microsoft.com/d89a0ee1-9a4b-48a4-8965-0d92f09743a6">STR_FILE_SYS_BIND_DATA</a> bind context parameter.


<a href="https://msdn.microsoft.com/d89a0ee1-9a4b-48a4-8965-0d92f09743a6">STR_PARSE_PREFER_FOLDER_BROWSING</a> can be passed to indicate that URLs are parsed using the file system data source when possible. Construct a bind context object using <a href="https://msdn.microsoft.com/0f0ded09-7a7c-40bb-8198-b9f5058827d4">CreateBindCtx</a> and populate the values using <a href="https://msdn.microsoft.com/7ee2b5b2-9b9c-41f1-8e58-7432ebc0f9ed">IBindCtx::RegisterObjectParam</a>. See <b>Bind Context String Keys</b> for a complete list of these. See the <a href="https://msdn.microsoft.com/FAC6099D-7631-49ac-B3A5-DBFF9B288C1D">Parsing With Parameters Sample</a> for an example of the use of this parameter.



If no data is being passed to or received from the parsing function, this value can be <b>NULL</b>.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically <b>IID_IShellItem</b> or <b>IID_IShellItem2</b>.


### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> or <a href="https://msdn.microsoft.com/e54d8385-ec67-4825-ad7c-431807a4fcb4">IShellItem2</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct <b>IID</b> based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.




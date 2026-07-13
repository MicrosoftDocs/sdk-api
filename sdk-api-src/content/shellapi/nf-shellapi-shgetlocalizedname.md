---
UID: NF:shellapi.SHGetLocalizedName
title: SHGetLocalizedName function (shellapi.h)
description: Retrieves the localized name of a file in a Shell folder.
helpviewer_keywords: ["SHGetLocalizedName","SHGetLocalizedName function [Windows Shell]","_shell_SHGetLocalizedName","shell.SHGetLocalizedName","shellapi/SHGetLocalizedName"]
old-location: shell\SHGetLocalizedName.htm
tech.root: shell
ms.assetid: 2929b77f-4467-44a8-9885-96f0c3e35584
ms.date: 12/05/2018
ms.keywords: SHGetLocalizedName, SHGetLocalizedName function [Windows Shell], _shell_SHGetLocalizedName, shell.SHGetLocalizedName, shellapi/SHGetLocalizedName
req.header: shellapi.h
req.include-header: 
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
req.lib: shell32.lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetLocalizedName
 - shellapi/SHGetLocalizedName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetLocalizedName
---

# SHGetLocalizedName function


## -description

Retrieves the localized name of a file in a Shell folder.

## -parameters

### -param pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a string that specifies the fully qualified path of the file.

### -param pszResModule [out]

Type: <b>PWSTR</b>

When this function returns, contains a pointer to a string resource that specifies the localized version of the file name.

### -param cch

Type: <b>UINT</b>

When this function returns, contains the size of the string, in <b>WCHARs</b>, at <i>pszResModule</i>.

### -param pidsRes [out]

Type: <b>int*</b>

When this function returns, contains a pointer to the ID of the localized file name in the resource file.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


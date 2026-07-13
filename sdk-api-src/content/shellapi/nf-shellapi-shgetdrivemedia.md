---
UID: NF:shellapi.SHGetDriveMedia
title: SHGetDriveMedia function (shellapi.h)
description: Returns the type of media that is in the given drive.
helpviewer_keywords: ["SHGetDriveMedia","SHGetDriveMedia function [Windows Shell]","_shell_SHGetDriveMedia","shell.SHGetDriveMedia","shellapi/SHGetDriveMedia"]
old-location: shell\SHGetDriveMedia.htm
tech.root: shell
ms.assetid: 9b1208cd-3c13-456a-8a7f-0f149cb86d38
ms.date: 12/05/2018
ms.keywords: SHGetDriveMedia, SHGetDriveMedia function [Windows Shell], _shell_SHGetDriveMedia, shell.SHGetDriveMedia, shellapi/SHGetDriveMedia
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
 - SHGetDriveMedia
 - shellapi/SHGetDriveMedia
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
 - SHGetDriveMedia
---

# SHGetDriveMedia function


## -description

Returns the type of media that is in the given drive.

## -parameters

### -param pszDrive [in]

Type: <b>PCWSTR</b>

The drive in which to check the media type.

### -param pdwMediaContent [out]

Type: <b>DWORD*</b>

A pointer to the type of media in the given drive. A combination of <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iquerycancelautoplay-allowautoplay">ARCONTENT</a> flags.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
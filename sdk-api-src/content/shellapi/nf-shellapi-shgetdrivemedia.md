---
UID: NF:shellapi.SHGetDriveMedia
title: SHGetDriveMedia function
author: windows-sdk-content
description: Returns the type of media that is in the given drive.
old-location: shell\SHGetDriveMedia.htm
old-project: shell
ms.assetid: 9b1208cd-3c13-456a-8a7f-0f149cb86d38
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SHGetDriveMedia, SHGetDriveMedia function [Windows Shell], _shell_SHGetDriveMedia, shell.SHGetDriveMedia, shellapi/SHGetDriveMedia
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SHSTOCKICONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetDriveMedia
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
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

A pointer to the type of media in the given drive. A combination of <a href="https://msdn.microsoft.com/ebc826a2-d7ea-413a-836b-c7e51f13692a">ARCONTENT</a> flags.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




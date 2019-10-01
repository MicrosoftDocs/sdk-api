---
UID: NF:shlwapi.SHOpenRegStream2A
title: SHOpenRegStream2A function (shlwapi.h)
author: windows-sdk-content
description: Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes SHOpenRegStream.
old-location: shell\SHOpenRegStream2.htm
tech.root: shell
ms.assetid: 2450dde0-cd02-4d48-be40-467b4b8be240
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SHOpenRegStream2, SHOpenRegStream2 function [Windows Shell], SHOpenRegStream2A, SHOpenRegStream2W, STGM_READ, STGM_READWRITE, STGM_WRITE, _win32_SHOpenRegStream2, shell.SHOpenRegStream2, shlwapi/SHOpenRegStream2, shlwapi/SHOpenRegStream2A, shlwapi/SHOpenRegStream2W
ms.topic: function
f1_keywords: 
 - "shlwapi/SHOpenRegStream2"
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHOpenRegStream2W (Unicode) and SHOpenRegStream2A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-stream-l1-1-0.dll
api_name:
 - SHOpenRegStream2
 - SHOpenRegStream2A
 - SHOpenRegStream2W
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHOpenRegStream2A function


## -description


Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes <a href="https://docs.microsoft.com/windows/desktop/api/shlwapi/nf-shlwapi-shopenregstreama">SHOpenRegStream</a>.


## -parameters




### -param hkey [in]

Type: <b>HKEY</b>

Required. The subtree, such as HKEY_LOCAL_MACHINE, that contains the value.


### -param pszSubkey [in, optional]

Type: <b>LPCTSTR</b>

Optional. Pointer to a null-terminated string that specifies the subkey that contains the value. This value can be <b>NULL</b>.


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that specifies the value to be accessed. This value can be <b>NULL</b>.


### -param grfMode [in]

Type: <b>DWORD</b>

The type of access for the stream. This can be one of the following values:



#### STGM_READ

Open the stream for reading.



#### STGM_WRITE

Open the stream for writing.



#### STGM_READWRITE

Open the stream for reading and writing.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Returns an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface pointer if successful; otherwise, <b>NULL</b>. A <b>NULL</b> value can be caused by several situations, including an invalid <i>hkey</i> or <i>pszSubkey</i>, a subkey named by <i>pszSubkey</i> that does not exist, a caller without sufficient permissions to access the subkey, or an inability to open the stream.




## -remarks



The calling application is responsible for calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method of the returned object when that <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> object is no longer needed.




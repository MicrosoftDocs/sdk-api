---
UID: NF:shlwapi.SHOpenRegStream2W
title: SHOpenRegStream2W function
author: windows-sdk-content
description: Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes SHOpenRegStream.
old-location: shell\SHOpenRegStream2.htm
old-project: shell
ms.assetid: 2450dde0-cd02-4d48-be40-467b4b8be240
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHOpenRegStream2, SHOpenRegStream2 function [Windows Shell], SHOpenRegStream2A, SHOpenRegStream2W, STGM_READ, STGM_READWRITE, STGM_WRITE, _win32_SHOpenRegStream2, shell.SHOpenRegStream2, shlwapi/SHOpenRegStream2, shlwapi/SHOpenRegStream2A, shlwapi/SHOpenRegStream2W
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
-	ShCore.dll
-	API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
-	API-MS-Win-ShCore-stream-l1-1-0.dll
api_name:
-	SHOpenRegStream2
-	SHOpenRegStream2A
-	SHOpenRegStream2W
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHOpenRegStream2W function


## -description


Opens a registry value and supplies a stream that can be used to read from or write to the value. This function supersedes <a href="https://msdn.microsoft.com/2f839b89-8584-4b4d-91e7-166b6e2b6892">SHOpenRegStream</a>.


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


##### - grfMode.STGM_READ

Open the stream for reading.


##### - grfMode.STGM_READWRITE

Open the stream for reading and writing.


##### - grfMode.STGM_WRITE

Open the stream for writing.


## -returns



Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Returns an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface pointer if successful; otherwise, <b>NULL</b>. A <b>NULL</b> value can be caused by several situations, including an invalid <i>hkey</i> or <i>pszSubkey</i>, a subkey named by <i>pszSubkey</i> that does not exist, a caller without sufficient permissions to access the subkey, or an inability to open the stream.




## -remarks



The calling application is responsible for calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method of the returned object when that <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object is no longer needed.




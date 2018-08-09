---
UID: NF:shlwapi.IStream_Write
title: IStream_Write function
author: windows-sdk-content
description: Writes data of unknown format from a buffer to a specified stream.
old-location: shell\IStream_Write.htm
old-project: shell
ms.assetid: fdcfdaf8-7fcb-433e-b3d4-98ca143fbe6b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IStream_Write, IStream_Write function [Windows Shell], _shell_IStream_Write, shell.IStream_Write, shlwapi/IStream_Write
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
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
tech.root: 
req.typenames: URL_SCHEME
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
 - IStream_Write
product: Windows
targetos: Windows
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IStream_Write function


## -description


Writes data of unknown format from a buffer to a specified stream.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer that specifies the target stream.


### -param pv [in]

Type: <b>const void*</b>

Pointer to a buffer that holds the data to send to the target stream. This buffer must be at least <i>cb</i> bytes in size.


### -param cb [in]

Type: <b>ULONG</b>

The number of bytes of data to write to the target stream.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the function successfully wrote the specified number of bytes to the stream, or an error value otherwise. In particular, if less than <i>cb</i> bytes was written to the target stream, even if some data was successfully written, the function returns E_FAIL.




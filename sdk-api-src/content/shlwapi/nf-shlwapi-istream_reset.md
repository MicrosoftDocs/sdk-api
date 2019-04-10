---
UID: NF:shlwapi.IStream_Reset
title: IStream_Reset function (shlwapi.h)
author: windows-sdk-content
description: Moves the seek position in a specified stream to the beginning of the stream.
old-location: shell\IStream_Reset.htm
tech.root: shell
ms.assetid: 1e7a881d-decb-4018-b2e8-e0cba454236d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStream_Reset, IStream_Reset function [Windows Shell], _win32_IStream_Reset, shell.IStream_Reset, shlwapi/IStream_Reset
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
 - IStream_Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStream_Reset function


## -description


Moves the seek position in a specified stream to the beginning of the stream.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface of the stream whose position is to be reset.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> on success or a COM failure code otherwise. See <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">IStream::Seek</a> for further discussion of possible error codes.




## -remarks



This function calls <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">IStream::Seek</a> to move the stream's seek position to the beginning of the stream.




---
UID: NF:shlwapi.IStream_Copy
title: IStream_Copy function
author: windows-sdk-content
description: Copies a stream to another stream.
old-location: shell\IStream_Copy.htm
old-project: shell
ms.assetid: 7d6a1080-dad4-4821-8f2a-bd1e01ca10cf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IStream_Copy, IStream_Copy function [Windows Shell], _shell_IStream_Copy, shell.IStream_Copy, shlwapi/IStream_Copy
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
 - IStream_Copy
product: Windows
targetos: Windows
req.lib: 
req.dll: Shlwapi.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IStream_Copy function


## -description


Copies a stream to another stream.


## -parameters




### -param pstmFrom [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the source stream.


### -param pstmTo [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the destination stream.


### -param cb [in]

Type: <b>DWORD</b>

The number of bytes to copy from the source stream.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




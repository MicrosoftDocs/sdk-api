---
UID: NF:shlwapi.IStream_Size
title: IStream_Size function
author: windows-sdk-content
description: Retrieves the size, in bytes, of a specified stream.
old-location: shell\IStream_Size.htm
old-project: shell
ms.assetid: 93c7c24d-6431-4859-b0b8-b36392bc5108
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IStream_Size, IStream_Size function [Windows Shell], _win32_IStream_Size, shell.IStream_Size, shlwapi/IStream_Size
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
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
 - IStream_Size
product: Windows
targetos: Windows
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IStream_Size function


## -description


Retrieves the size, in bytes, of a specified stream.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface of the stream whose size is to be determined.


### -param pui [out]

Type: <b><a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> structure to receive the size of the stream.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> on success or a COM failure code otherwise. See <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a> for further discussion of possible error codes.




## -remarks



This function gets the size of the stream by calling the specified stream object's <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">IStream::Stat</a> method. It then copies the value of the <b>cbSize</b> member of the <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure returned by <b>IStream::Stat</b> to the <a href="https://msdn.microsoft.com/83a10c12-2cd1-449a-af3f-b2138fc50ee0">ULARGE_INTEGER</a> structure pointed to by <i>pui</i>.  If the function fails, the contents of the <b>ULARGE_INTEGER</b> structure are undefined.




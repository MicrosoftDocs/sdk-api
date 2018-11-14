---
UID: NF:appxpackaging.IAppxFile.GetStream
title: IAppxFile::GetStream
author: windows-sdk-content
description: Gets a read-only stream that contains the uncompressed content of the file.
old-location: appxpkg\iappxfile_getstream.htm
tech.root: appxpkg
ms.assetid: B002A9A9-0BF5-4FB1-8D7D-06F7D066432C
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetStream, GetStream method [App packaging and management], GetStream method [App packaging and management],IAppxFile interface, IAppxFile interface [App packaging and management],GetStream method, IAppxFile.GetStream, IAppxFile::GetStream, appxpackaging/IAppxFile::GetStream, appxpkg.iappxfile_getstream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFile.GetStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- appxpackaging.h
: 
- IAppxFile.GetStream
: 
---

# IAppxFile::GetStream


## -description


Gets a read-only stream that contains the uncompressed content of the file.


## -parameters




### -param stream [out, retval]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

A read-only stream that contains the uncompressed content of the file.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. 

[Fatal] OPC error codes (0x8051xxxx) if the file’s local file header or data descriptor in the zip archive is invalid.  This failure causes the entire OPC zip consumer to enter an invalid state, no other file can be accessed from the <a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a> object after this error occurs.

HRESULT_FROM_WIN32(ERROR_CRC) (0x80070017) if the stream has been previously read and its CRC was invalid.

<b>Return value from the returned IStream’s Read and CopyTo methods</b>

[Fatal] HRESULT_FROM_WIN32(ERROR_CRC) (0x80070017) if the entire stream has been read and its CRC is found to be invalid

APPX_E_CORRUPT_CONTENT (0x80080206) if the file content can't be decompressed (due to corruption of the zip file)


HRESULT_FROM_WIN32(ERROR_INVALID_DATA) (0x8007000d) if a block in the file can't be read completely or the size of the block is unexpected

APPX_E_BLOCK_HASH_INVALID (0x80080207) if the content of this file’s blocks is inconsistent with its hash in the block map




## -remarks



The <i>stream</i> returned is read-only and cloneable.

Validation of payload files is "lazy."  On the first call to the file’s <b>GetStream</b> method, the corresponding zip file item’s local file header and data descriptor is validated and might cause <b>GetStream</b> to fail.  Subsequent calls to <b>GetStream</b> on the same file don't repeat these validations.  The zip file item’s CRC checksum is only validated if the stream is read in its entirety in sequential order.


Instances of <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that are returned for payload files are optimized for sequential access.  While random access to the stream is supported, that random access might be slower and more CPU-intensive.  We recommend a single sequential read of these streams whenever possible.  Reading the same range multiple times is supported but not recommended for performance; consider caching such ranges if their usage scenario demands it.





## -see-also




<a href="https://msdn.microsoft.com/DB09452D-725C-46EA-B74C-92C5E596BEF8">IAppxFile</a>



<a href="https://msdn.microsoft.com/D34D0909-BE2B-4182-8C3D-36A4E8DDC820">IAppxPackageReader</a>
 

 


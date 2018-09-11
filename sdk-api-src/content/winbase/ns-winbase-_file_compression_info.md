---
UID: NS:winbase._FILE_COMPRESSION_INFO
title: "_FILE_COMPRESSION_INFO"
author: windows-sdk-content
description: Receives file compression information.
old-location: fs\file_compression_info.htm
tech.root: fileio
ms.assetid: 2f64e7cc-e23c-4e3d-8e17-0e8e38f1ea24
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PFILE_COMPRESSION_INFO, FILE_COMPRESSION_INFO, FILE_COMPRESSION_INFO structure [Files], PFILE_COMPRESSION_INFO, PFILE_COMPRESSION_INFO structure pointer [Files], _FILE_COMPRESSION_INFO, fileextd/FILE_COMPRESSION_INFO, fileextd/PFILE_COMPRESSION_INFO, fs.file_compression_info, winbase/FILE_COMPRESSION_INFO, winbase/PFILE_COMPRESSION_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - FileExtd.h
api_name:
 - FILE_COMPRESSION_INFO
product: Windows
targetos: Windows
req.typenames: FILE_COMPRESSION_INFO, *PFILE_COMPRESSION_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
---

# _FILE_COMPRESSION_INFO structure


## -description


Receives file compression information. Used for any handles. Use only when calling <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>.


## -struct-fields




### -field CompressedFileSize

The file size of the compressed file.


### -field CompressionFormat

The compression format that is used to compress the file.


### -field CompressionUnitShift

The factor that the compression uses.


### -field ChunkShift

The number of chunks that are shifted by compression.


### -field ClusterShift

The number of clusters that are shifted by compression.


### -field Reserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 


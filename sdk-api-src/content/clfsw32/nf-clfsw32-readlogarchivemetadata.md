---
UID: NF:clfsw32.ReadLogArchiveMetadata
title: ReadLogArchiveMetadata function
author: windows-sdk-content
description: Copies a range of the archive view of the metadata to the specified buffer.
old-location: fs\readlogarchivemetadata.htm
old-project: Clfs
ms.assetid: b0b8528d-30fc-4995-b82d-5577af8d299d
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ReadLogArchiveMetadata, ReadLogArchiveMetadata function [Files], clfsw32/ReadLogArchiveMetadata, fs.readlogarchivemetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	ReadLogArchiveMetadata
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# ReadLogArchiveMetadata function


## -description


Copies a range of the archive view of the metadata to the specified buffer.


## -parameters




### -param pvArchiveContext [in]

A pointer to an  archive context that is obtained by a call to <a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a>.

  The context maintains  the cursor state, which allows iteration through the set of file extents in the archive.  The archive client is responsible for deallocating the context by using the <a href="https://msdn.microsoft.com/885356e1-f7c4-4f3f-98c3-fb9b1d339e22">TerminateLogArchive</a> function.


### -param cbOffset [in]

The offset in the metadata where data copying starts.  

On the first call to this function, specify zero (0). On subsequent calls, specify the value that is returned in <i>pcbBytesRead</i>.


### -param cbBytesToRead [in]

The number of bytes of the metadata snapshot should be copied into <i>pbReadBuffer</i>.  

This parameter cannot be zero (0).


### -param pbReadBuffer [in, out]

A pointer to the buffer  where the metadata snapshot is copied.


### -param pcbBytesRead [out]

A pointer to a variable that receives the number of bytes  that are  copied to <i>pbReadBuffer</i>.  

The number of bytes is always between zero (0) and <i>cbBytesToRead</i>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies  the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a>



<a href="https://msdn.microsoft.com/885356e1-f7c4-4f3f-98c3-fb9b1d339e22">TerminateLogArchive</a>
 

 


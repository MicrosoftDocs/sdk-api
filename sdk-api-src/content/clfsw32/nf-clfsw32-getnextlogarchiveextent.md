---
UID: NF:clfsw32.GetNextLogArchiveExtent
title: GetNextLogArchiveExtent function
author: windows-sdk-content
description: Retrieves the next set of archive extents in a log archive context.
old-location: fs\getnextlogarchiveextent.htm
old-project: Clfs
ms.assetid: 4aaf10bd-e9df-435b-a756-5ae5c1eb2903
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetNextLogArchiveExtent, GetNextLogArchiveExtent function [Files], clfsw32/GetNextLogArchiveExtent, fs.getnextlogarchiveextent
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	GetNextLogArchiveExtent
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# GetNextLogArchiveExtent function


## -description


Retrieves the next set of archive extents in a log archive context.  The log archive context describes a   contiguous set of file extents that span the snapshot of the active log  captured by  <a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a> captures.  <b>GetNextLogArchiveExtent</b> maintains a cursor in the ordered set of log archive descriptors so that  subsequent calls allow an application to iterate through the entire set.


## -parameters




### -param pvArchiveContext [in]

A pointer to an  archive context that is obtained by a call to <a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a>.

  The context maintains  the cursor state, which allows iteration through the set of file extents in the archive.  The archive client is responsible for deallocating the context by using the <a href="https://msdn.microsoft.com/885356e1-f7c4-4f3f-98c3-fb9b1d339e22">TerminateLogArchive</a> function.


### -param rgadExtent [in, out]

A client-allocated array of <a href="https://msdn.microsoft.com/a2d50d1d-f4cb-48de-be73-4858adfa951f">CLFS_ARCHIVE_DESCRIPTOR</a>  structures to be filled in by this function.


### -param cDescriptors [in]

The number of elements in  the <i>rgadExtent</i> array. 

This value is the maximum number of archive descriptors that can be retrieved by this function.


### -param pcDescriptorsReturned [out]

The number of descriptors in the <i>rgadExtent</i> array that are  filled in by this function.  

If this value is less than <i>cDescriptors</i>,  the set of descriptors is exhausted and the archive client can terminate iteration through the ordered descriptor set.  Further calls to this function fail with ERROR_NO_MORE_ENTRIES.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/a2d50d1d-f4cb-48de-be73-4858adfa951f">CLFS_ARCHIVE_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 


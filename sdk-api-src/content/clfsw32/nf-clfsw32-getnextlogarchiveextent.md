---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


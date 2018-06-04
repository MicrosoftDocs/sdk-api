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

# MsiRecordSetStreamA function


## -description


The 
<b>MsiRecordSetStream</b> function sets a record stream field from a file. Stream data cannot be inserted into temporary fields.


## -parameters




### -param hRecord [in]

Handle to the record.


### -param iField [in]

Specifies the field of the record to set.


### -param szFilePath [in]

Specifies the path to the file containing the stream.


## -returns




					The 
<b>MsiRecordSetStream</b> function returns the following values:




## -remarks



The contents of the file specified in the 
<b>MsiRecordSetStream</b> function is read into a stream object. The stream persists if the record is inserted into the database and the database is committed.

To reset the stream to its beginning you must pass in a Null pointer for <i>szFilePath</i>. Do not pass a pointer to an empty string, "", to reset the stream.

See also 
<a href="https://msdn.microsoft.com/ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef">OLE Limitations on Streams</a>.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">Record Processing Functions</a>
 

 


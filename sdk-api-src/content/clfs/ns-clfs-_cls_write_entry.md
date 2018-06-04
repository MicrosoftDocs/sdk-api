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

# _CLS_WRITE_ENTRY structure


## -description


Contains  a user buffer, which is to become part of a log record, and its length.  The <a href="https://msdn.microsoft.com/2036fc26-d040-4738-b66e-d5d3d0dbe385">ReserveAndAppendLog</a> function uses <b>CLFS_WRITE_ENTRY</b> structures  in  the  routine that appends log records to logs. This routine requires the client to specify a set of structures.  <b>ReserveAndAppendLog</b> gathers these structures and  formats them into a log record in a marshaling buffer,  which is eventually flushed to the log.


## -struct-fields




### -field Buffer

The log record data buffer.


### -field ByteLength

The length of the log record data buffer, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/2036fc26-d040-4738-b66e-d5d3d0dbe385">ReserveAndAppendLog</a>
 

 


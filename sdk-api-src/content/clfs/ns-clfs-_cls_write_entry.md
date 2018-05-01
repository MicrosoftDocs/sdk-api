---
UID: NS:clfs._CLS_WRITE_ENTRY
title: "_CLS_WRITE_ENTRY"
author: windows-driver-content
description: Contains a user buffer, which is to become part of a log record, and its length.
old-location: fs\clfs_write_entry.htm
old-project: Clfs
ms.assetid: 7c81a695-b93c-4c74-8ee8-133eea9f12d9
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: "*PCLFS_WRITE_ENTRY, *PCLS_WRITE_ENTRY, CLFS_WRITE_ENTRY, CLFS_WRITE_ENTRY structure [Files], CLS_WRITE_ENTRY, PCLFS_WRITE_ENTRY, PCLFS_WRITE_ENTRY structure pointer [Files], PPCLS_WRITE_ENTRY, _CLS_WRITE_ENTRY, clfs/PCLFS_WRITE_ENTRY, clfs/_CLFS_WRITE_ENTRY, fs.clfs_write_entry"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: clfs.h
req.include-header: Clfsw32.h
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
req.typenames: CLS_WRITE_ENTRY, *PCLS_WRITE_ENTRY, PPCLS_WRITE_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Clfs.h
api_name:
-	CLFS_WRITE_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 


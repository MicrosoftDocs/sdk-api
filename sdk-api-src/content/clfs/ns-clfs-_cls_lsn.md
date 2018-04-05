---
UID: NS:clfs._CLS_LSN
title: "_CLS_LSN"
author: windows-driver-content
description: Represents a valid log address.
old-location: fs\clfs_lsn.htm
old-project: Clfs
ms.assetid: f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PCLFS_LSN, *PCLS_LSN, CLFS_LSN, CLFS_LSN union [Files], CLS_LSN, PCLFS_LSN, PCLFS_LSN union pointer [Files], PPCLS_LSN, _CLS_LSN, clfs/CLFS_LSN, clfs/PCLFS_LSN, fs.clfs_lsn"
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
req.typenames: CLS_LSN, *PCLS_LSN, PPCLS_LSN
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Clfs.h
api_name:
-	CLFS_LSN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CLS_LSN structure


## -description


Represents a valid log address.


## -struct-fields




### -field Internal

The log sequence number (LSN).


## -remarks



The LSN is the valid address that is  unique to a client, and returned after the client appends a record to the log.  The address remains valid if the system does not fail, or its marshaled log buffer is  flushed successfully to disk.

In log streams, LSNs increase  monotonically. You cannot compare  LSNs between  log streams.




## -see-also




<a href="https://msdn.microsoft.com/3662ac53-25d5-4d8c-8f98-02f313e03dce">LsnCreate</a>
 

 


---
UID: NF:clfsw32.LsnCreate
title: LsnCreate function
author: windows-sdk-content
description: Creates a log sequence number (LSN), given a container ID, a block offset, and a record sequence number.
old-location: fs\lsncreate.htm
old-project: Clfs
ms.assetid: 3662ac53-25d5-4d8c-8f98-02f313e03dce
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: LsnCreate, LsnCreate function [Files], clfsw32/LsnCreate, fs.lsncreate
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - LsnCreate
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# LsnCreate function


## -description


Creates a log sequence number (LSN), given a container ID, a block offset, and a record sequence number.


## -parameters




### -param cidContainer [in]

The container ID. This value must be an integer between 0x0 and 0xFFFFFFFF.


### -param offBlock [in]

The block offset. This value must be a multiple of 512.


### -param cRecord [in]

The record sequence number. This value must be  an integer between  0 - 511.


## -returns



Returns a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure that represents the container ID, block offset, and record sequence number that is supplied by the caller.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/72445d03-1b9a-48a6-993e-792e1f524f4b">LsnBlockOffset</a>



<a href="https://msdn.microsoft.com/1bbbb37b-8197-44bd-b19b-c43ece1c46d2">LsnContainer</a>



<a href="https://msdn.microsoft.com/90aa2df8-328d-404c-a145-ad500a6e611a">LsnRecordSequence</a>
 

 


---
UID: NF:clfsw32.LsnRecordSequence
title: LsnRecordSequence function
author: windows-sdk-content
description: Retrieves the record sequence number that is contained in a specified LSN.
old-location: fs\lsnrecordsequence.htm
tech.root: Clfs
ms.assetid: 90aa2df8-328d-404c-a145-ad500a6e611a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LsnRecordSequence, LsnRecordSequence function [Files], clfsw32/LsnRecordSequence, fs.lsnrecordsequence
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - LsnRecordSequence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsnRecordSequence function


## -description


Retrieves the record sequence number that is contained in a specified LSN.


## -parameters




### -param plsn [in]

A pointer to a <a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a> structure from which the record sequence number is to be retrieved.


## -returns



The record sequence number that is contained in <i>plsn</i>.




## -see-also




<a href="https://msdn.microsoft.com/72445d03-1b9a-48a6-993e-792e1f524f4b">LsnBlockOffset</a>



<a href="https://msdn.microsoft.com/1bbbb37b-8197-44bd-b19b-c43ece1c46d2">LsnContainer</a>



<a href="https://msdn.microsoft.com/3662ac53-25d5-4d8c-8f98-02f313e03dce">LsnCreate</a>
 

 


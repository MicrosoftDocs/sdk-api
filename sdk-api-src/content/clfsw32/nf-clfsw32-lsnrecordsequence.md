---
UID: NF:clfsw32.LsnRecordSequence
title: LsnRecordSequence function (clfsw32.h)

description: Retrieves the record sequence number that is contained in a specified LSN.
old-location: fs\lsnrecordsequence.htm
tech.root: Clfs
ms.assetid: 90aa2df8-328d-404c-a145-ad500a6e611a

ms.date: 12/05/2018
ms.keywords: LsnRecordSequence, LsnRecordSequence function [Files], clfsw32/LsnRecordSequence, fs.lsnrecordsequence
ms.topic: function
f1_keywords:
- clfsw32/LsnRecordSequence
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LsnRecordSequence function


## -description


Retrieves the record sequence number that is contained in a specified LSN.


## -parameters




### -param plsn [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure from which the record sequence number is to be retrieved.


## -returns



The record sequence number that is contained in <i>plsn</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clfsw32/nf-clfsw32-lsnblockoffset">LsnBlockOffset</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfsw32/nf-clfsw32-lsncontainer">LsnContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfsw32/nf-clfsw32-lsncreate">LsnCreate</a>
 

 


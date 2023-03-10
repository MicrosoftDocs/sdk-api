---
UID: NF:clfsw32.LsnCreate
title: LsnCreate function (clfsw32.h)
description: Creates a log sequence number (LSN), given a container ID, a block offset, and a record sequence number.
helpviewer_keywords: ["LsnCreate","LsnCreate function [Files]","clfsw32/LsnCreate","fs.lsncreate"]
old-location: fs\lsncreate.htm
tech.root: fs
ms.assetid: 3662ac53-25d5-4d8c-8f98-02f313e03dce
ms.date: 12/05/2018
ms.keywords: LsnCreate, LsnCreate function [Files], clfsw32/LsnCreate, fs.lsncreate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsnCreate
 - clfsw32/LsnCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - LsnCreate
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

Returns a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that represents the container ID, block offset, and record sequence number that is supplied by the caller.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsnblockoffset">LsnBlockOffset</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsncontainer">LsnContainer</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsnrecordsequence">LsnRecordSequence</a>
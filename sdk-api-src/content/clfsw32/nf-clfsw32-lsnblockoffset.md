---
UID: NF:clfsw32.LsnBlockOffset
title: LsnBlockOffset function (clfsw32.h)
description: Returns the sector-aligned block offset that is contained in the specified LSN.
helpviewer_keywords: ["LsnBlockOffset","LsnBlockOffset function [Files]","clfsw32/LsnBlockOffset","fs.lsnblockoffset"]
old-location: fs\lsnblockoffset.htm
tech.root: fs
ms.assetid: 72445d03-1b9a-48a6-993e-792e1f524f4b
ms.date: 12/05/2018
ms.keywords: LsnBlockOffset, LsnBlockOffset function [Files], clfsw32/LsnBlockOffset, fs.lsnblockoffset
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
 - LsnBlockOffset
 - clfsw32/LsnBlockOffset
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
 - LsnBlockOffset
---

# LsnBlockOffset function


## -description

Returns the sector-aligned block offset that is contained in the specified LSN.

## -parameters

### -param plsn [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure from which the block offset is to be retrieved.

## -returns

<b>LsnBlockOffset</b> returns the block offset that is contained in <i>plsn</i>.

## -remarks

The block offset that is returned by this function is a multiple of the sector size on the stable storage medium. For example, if the sector size is 1024 bytes, the block offset is a multiple of 1024.


#### Examples

For an example that uses this function, see <a href="/previous-versions/windows/desktop/clfs/enumerating-log-containers">Enumerating Log Containers</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsncontainer">LsnContainer</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsncreate">LsnCreate</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsnrecordsequence">LsnRecordSequence</a>
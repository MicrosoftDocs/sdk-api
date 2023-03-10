---
UID: NF:clfsw32.LsnContainer
title: LsnContainer function (clfsw32.h)
description: Retrieves the logical container ID that is contained in a specified LSN.
helpviewer_keywords: ["LsnContainer","LsnContainer function [Files]","clfsw32/LsnContainer","fs.lsncontainer"]
old-location: fs\lsncontainer.htm
tech.root: fs
ms.assetid: 1bbbb37b-8197-44bd-b19b-c43ece1c46d2
ms.date: 12/05/2018
ms.keywords: LsnContainer, LsnContainer function [Files], clfsw32/LsnContainer, fs.lsncontainer
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
 - LsnContainer
 - clfsw32/LsnContainer
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
 - LsnContainer
---

# LsnContainer function


## -description

Retrieves the logical container ID that is contained in a specified LSN.

## -parameters

### -param plsn [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure from which the container ID is to be retrieved.

## -returns

This function returns the logical container ID that is contained in <i>plsn</i>. The logical container ID is not necessarily the same as the ID of the physical container on stable storage.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsnblockoffset">LsnBlockOffset</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsncreate">LsnCreate</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsnrecordsequence">LsnRecordSequence</a>
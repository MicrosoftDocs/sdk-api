---
UID: NF:clfs.ClfsLsnEqual
title: ClfsLsnEqual function (clfs.h)
description: Determines whether two LSNs from the same stream are equal.
helpviewer_keywords: ["ClfsLsnEqual","LsnEqual","LsnEqual function [Files]","clfs/LsnEqual","fs.lsnequal"]
old-location: fs\lsnequal.htm
tech.root: fs
ms.assetid: 995b3afd-5724-40d1-ab80-f2c7b2ea8560
ms.date: 12/05/2018
ms.keywords: ClfsLsnEqual, LsnEqual, LsnEqual function [Files], clfs/LsnEqual, fs.lsnequal
req.header: clfs.h
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
 - ClfsLsnEqual
 - clfs/ClfsLsnEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-fs-clfs-l1-1-0.dll
 - Clfsw32.dll
api_name:
 - LsnEqual
---

# ClfsLsnEqual function


## -description

Determines whether two LSNs from the same stream are equal.

## -parameters

### -param plsn1 [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to be compared with  <i>plsn2</i>.

### -param plsn2 [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to be compared with  <i>plsn1</i>.

## -returns

Returns <b>TRUE</b> if the two LSNs are equal; otherwise,  <b>FALSE</b>.

## -remarks

CLFS_LSN_NULL (the smallest LSN) and CLFS_LSN_INVALID (larger than any valid LSN) are valid arguments to this function.

LSNs from different streams are not comparable. Do not use this function to compare LSNs from different streams.

## -see-also

<a href="/windows/desktop/api/clfs/nf-clfs-clfslsngreater">LsnGreater</a>



<a href="/windows/desktop/api/clfs/nf-clfs-clfslsnless">LsnLess</a>



<a href="/windows/desktop/api/clfs/nf-clfs-clfslsnnull">LsnNull</a>
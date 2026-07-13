---
UID: NF:clfs.ClfsLsnGreater
title: ClfsLsnGreater function (clfs.h)
description: Determines whether one LSN is greater than another LSN. The two LSNs must be from the same stream.
helpviewer_keywords: ["ClfsLsnGreater","LsnGreater","LsnGreater function [Files]","clfs/LsnGreater","fs.lsngreater"]
old-location: fs\lsngreater.htm
tech.root: fs
ms.assetid: 15657fc4-40f6-4f89-89b4-ff51d72d5e74
ms.date: 12/05/2018
ms.keywords: ClfsLsnGreater, LsnGreater, LsnGreater function [Files], clfs/LsnGreater, fs.lsngreater
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
 - ClfsLsnGreater
 - clfs/ClfsLsnGreater
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
 - LsnGreater
---

# ClfsLsnGreater function


## -description

Determines whether one LSN is greater than another LSN. The two LSNs must be from the same stream.

## -parameters

### -param plsn1 [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to be compared with  <i>plsn2</i>.

### -param plsn2 [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to be compared with  <i>plsn1</i>.

## -returns

<b>TRUE</b> if <i>plsn1</i> is strictly greater than <i>plsn2</i>; otherwise,  <b>FALSE</b>.

## -remarks

CLFS_LSN_NULL (the smallest LSN) and CLFS_LSN_INVALID (larger than any valid LSN) are valid arguments to this function.

LSNs from different streams are not comparable. Do not use this function to compare LSNs from different streams.

## -see-also

<a href="/windows/desktop/api/clfs/nf-clfs-clfslsnequal">LsnEqual</a>



<a href="/windows/desktop/api/clfs/nf-clfs-clfslsnless">LsnLess</a>



<a href="/windows/desktop/api/clfs/nf-clfs-clfslsnnull">LsnNull</a>
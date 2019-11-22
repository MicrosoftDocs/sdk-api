---
UID: NF:clfs.ClfsLsnLess
title: ClfsLsnLess function (clfs.h)

description: Determines whether one LSN is less than another LSN. The two LSNs must be from the same stream.
old-location: fs\lsnless.htm
tech.root: Clfs
ms.assetid: 610023f3-6017-480f-9a0c-807e81a50e84

ms.date: 12/05/2018
ms.keywords: ClfsLsnLess, LsnLess, LsnLess function [Files], clfs/LsnLess, fs.lsnless
ms.topic: function
f1_keywords:
- clfs/LsnLess
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Clfsw32.dll
api_name:
- LsnLess
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClfsLsnLess function


## -description


Determines whether one LSN is less than another LSN. The two LSNs must be from the same stream.


## -parameters




### -param plsn1 [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to be compared with  <i>plsn2</i>.


### -param plsn2 [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to be compared with  <i>plsn1</i>.


## -returns



<b>TRUE</b> if <i>plsn1</i> is strictly less than <i>plsn2</i>; otherwise,  <b>FALSE</b>.




## -remarks



CLFS_LSN_NULL (the smallest LSN) and CLFS_LSN_INVALID (larger than any valid LSN) are valid arguments to this function.

LSNs from different streams are not comparable. Do not use this function to compare LSNs from different streams.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clfs/nf-clfs-clfslsnequal">LsnEqual</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfs/nf-clfs-clfslsngreater">LsnGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfs/nf-clfs-clfslsnnull">LsnNull</a>
 

 


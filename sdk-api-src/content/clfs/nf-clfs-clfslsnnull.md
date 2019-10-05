---
UID: NF:clfs.ClfsLsnNull
title: ClfsLsnNull function (clfs.h)
author: windows-sdk-content
description: Determines whether a specified LSN is equal to the smallest possible LSN, which is CLFS_LSN_NULL.
old-location: fs\lsnnull.htm
tech.root: Clfs
ms.assetid: effa7924-fcde-4aaf-964b-a6916cb6d1f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClfsLsnNull, LsnNull, LsnNull function [Files], clfs/LsnNull, fs.lsnnull
ms.topic: function
f1_keywords:
- clfs/LsnNull
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
- LsnNull
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClfsLsnNull function


## -description


Determines whether a specified LSN is equal to the smallest possible LSN, which is CLFS_LSN_NULL.


## -parameters




### -param plsn [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to be tested.


## -returns



<b>TRUE</b> if <i>plsn</i> is equal to CLFS_LSN_NULL; otherwise,  <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clfs/nf-clfs-clfslsnequal">LsnEqual</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfs/nf-clfs-clfslsngreater">LsnGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfs/nf-clfs-clfslsnless">LsnLess</a>
 

 


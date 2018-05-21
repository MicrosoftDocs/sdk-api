---
UID: NF:clfs.ClfsLsnEqual
title: ClfsLsnEqual function
author: windows-driver-content
description: Determines whether two LSNs from the same stream are equal.
old-location: fs\lsnequal.htm
old-project: Clfs
ms.assetid: 995b3afd-5724-40d1-ab80-f2c7b2ea8560
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ClfsLsnEqual, LsnEqual, LsnEqual function [Files], clfs/LsnEqual, fs.lsnequal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: CLFS_LOG_ARCHIVE_MODE, *PCLFS_LOG_ARCHIVE_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	LsnEqual
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# ClfsLsnEqual function


## -description


Determines whether two LSNs from the same stream are equal.


## -parameters




### -param plsn1 [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure to be compared with  <i>plsn2</i>.


### -param plsn2 [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure to be compared with  <i>plsn1</i>.


## -returns



Returns <b>TRUE</b> if the two LSNs are equal; otherwise,  <b>FALSE</b>.





## -remarks



CLFS_LSN_NULL (the smallest LSN) and CLFS_LSN_INVALID (larger than any valid LSN) are valid arguments to this function.

LSNs from different streams are not comparable. Do not use this function to compare LSNs from different streams.




## -see-also




<a href="https://msdn.microsoft.com/15657fc4-40f6-4f89-89b4-ff51d72d5e74">LsnGreater</a>



<a href="https://msdn.microsoft.com/610023f3-6017-480f-9a0c-807e81a50e84">LsnLess</a>



<a href="https://msdn.microsoft.com/effa7924-fcde-4aaf-964b-a6916cb6d1f5">LsnNull</a>
 

 


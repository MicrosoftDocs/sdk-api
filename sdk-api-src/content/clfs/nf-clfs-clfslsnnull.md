---
UID: NF:clfs.ClfsLsnNull
title: ClfsLsnNull function
author: windows-sdk-content
description: Determines whether a specified LSN is equal to the smallest possible LSN, which is CLFS_LSN_NULL.
old-location: fs\lsnnull.htm
old-project: Clfs
ms.assetid: effa7924-fcde-4aaf-964b-a6916cb6d1f5
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ClfsLsnNull, LsnNull, LsnNull function [Files], clfs/LsnNull, fs.lsnnull
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CLFS_LOG_ARCHIVE_MODE, *PCLFS_LOG_ARCHIVE_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - LsnNull
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# ClfsLsnNull function


## -description


Determines whether a specified LSN is equal to the smallest possible LSN, which is CLFS_LSN_NULL.


## -parameters




### -param plsn [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure to be tested.


## -returns



<b>TRUE</b> if <i>plsn</i> is equal to CLFS_LSN_NULL; otherwise,  <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/995b3afd-5724-40d1-ab80-f2c7b2ea8560">LsnEqual</a>



<a href="https://msdn.microsoft.com/15657fc4-40f6-4f89-89b4-ff51d72d5e74">LsnGreater</a>



<a href="https://msdn.microsoft.com/610023f3-6017-480f-9a0c-807e81a50e84">LsnLess</a>
 

 


---
UID: NF:filehc.InsertFile
title: InsertFile function (filehc.h)
description: Inserts a file into the cache.
helpviewer_keywords: ["InsertFile","InsertFile function [Windows API]","filehc/InsertFile","winprog._insertfile"]
old-location: winprog\_insertfile.htm
tech.root: winprog
ms.assetid: 5461dc96-a625-43d7-87e7-c25389e9c822
ms.date: 12/05/2018
ms.keywords: InsertFile, InsertFile function [Windows API], filehc/InsertFile, winprog._insertfile
f1_keywords:
- filehc/InsertFile
dev_langs:
- c++
req.header: filehc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Fcachdll.dll
api_name:
- InsertFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InsertFile function


## -description


Inserts a file into the cache.


## -parameters




### -param lpstrName [in]

The name of the file to be inserted.


### -param pContext [in]

A pointer to the <a href="https://msdn.microsoft.com/library/ms528326.aspx">FIO_CONTEXT</a> structure that is associated with the file being inserted.


### -param fKeepReference [in]

Specifies whether the reference to the file is to be kept. If <b>TRUE</b>, the user must make a call to <a href="https://msdn.microsoft.com/library/ms527734.aspx">ReleaseContext</a> for the inserted <a href="https://msdn.microsoft.com/library/ms528326.aspx">FIO_CONTEXT</a>.


## -returns



Returns <b>TRUE</b> if the file is inserted; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms528326.aspx">FIO_CONTEXT</a>



<a href="https://msdn.microsoft.com/library/ms527734.aspx">ReleaseContext</a>
 

 


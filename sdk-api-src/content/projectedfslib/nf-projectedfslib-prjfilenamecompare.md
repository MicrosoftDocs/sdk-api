---
UID: NF:projectedfslib.PrjFileNameCompare
title: PrjFileNameCompare function (projectedfslib.h)
description: Compares two file names and returns a value that indicates their relative collation order.
old-location: projfs\prjfilenamecompare.htm
tech.root: ProjFS
ms.assetid: A20C2E31-918D-4AE8-9C54-D88BB5DC21E7
ms.date: 12/05/2018
ms.keywords: PrjFileNameCompare, PrjFileNameCompare function, ProjFS.prjfilenamecompare, projectedfslib/PrjFileNameCompare
ms.topic: function
f1_keywords:
- projectedfslib/PrjFileNameCompare
dev_langs:
- c++
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- projectedfslib.h
api_name:
- PrjFileNameCompare
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# PrjFileNameCompare function


## -description


Compares two file names and returns a value that indicates their relative collation order.


## -parameters




### -param fileName1 [in]

A null-terminated Unicode string specifying the first name to compare.


### -param fileName2 [in]

A null-terminated Unicode string specifying the second name to compare.


## -returns



<ul>
<li>&lt;0 indicates fileName1 is before fileName2 in collation order</li>
<li>0 indicates fileName1 is equal to fileName2</li>
<li>&gt;0 indicates fileName1 is after fileName2 in collation order</li>
</ul>



## -remarks



The provider may use this routine to determine how to sort file names in the same order that the file system does.




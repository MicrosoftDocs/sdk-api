---
UID: NF:projectedfslib.PrjFileNameMatch
title: PrjFileNameMatch function (projectedfslib.h)
description: Determines whether a file name matches a search pattern.
helpviewer_keywords: ["PrjFileNameMatch","PrjFileNameMatch function","ProjFS.prjfilenamematch","projectedfslib/PrjFileNameMatch"]
old-location: projfs\prjfilenamematch.htm
tech.root: ProjFS
ms.assetid: 2BE57189-0F68-4CCD-8796-964EFDE0A02E
ms.date: 12/05/2018
ms.keywords: PrjFileNameMatch, PrjFileNameMatch function, ProjFS.prjfilenamematch, projectedfslib/PrjFileNameMatch
f1_keywords:
- projectedfslib/PrjFileNameMatch
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
- PrjFileNameMatch
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# PrjFileNameMatch function


## -description


Determines whether a file name matches a search pattern.


## -parameters




### -param fileNameToCheck [in]

A null-terminated Unicode string of at most MAX_PATH characters specifying the file name to check against pattern. 


### -param pattern [in]

A null-terminated Unicode string of at most MAX_PATH characters specifying the pattern to compare against fileNameToCheck.


## -returns



True if fileNameToCheck matches pattern, False otherwise.




## -remarks



The provider must use this routine when processing a <a href="https://docs.microsoft.com/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb">PRJ_GET_DIRECTORY_ENUMERATION_CB</a> callback to determine whether a name in its backing store matches the searchExpression passed to the callback. This routine performs pattern matching in the same way the file system does when it is processing a directory enumeration




---
UID: NS:docobj.tagPAGESET
title: PAGESET (docobj.h)
description: Identifies one or more page-ranges to be printed and, optionally, identifies only the even or odd pages as part of a pageset.
helpviewer_keywords: ["PAGESET","PAGESET structure [COM]","_ctrl_PAGESET","com.pageset","docobj/PAGESET"]
old-location: com\pageset.htm
tech.root: com
ms.assetid: 9639c743-2509-4611-833b-16d16fce420a
ms.date: 12/05/2018
ms.keywords: PAGESET, PAGESET structure [COM], _ctrl_PAGESET, com.pageset, docobj/PAGESET
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: PAGESET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPAGESET
 - docobj/tagPAGESET
 - PAGESET
 - docobj/PAGESET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Docobj.h
api_name:
 - PAGESET
---

# PAGESET structure


## -description

Identifies one or more page-ranges to be printed and, optionally, identifies only the even or odd pages as part of a pageset.

## -struct-fields

### -field cbStruct

The number of bytes in this instance of the <b>PAGESET</b> structure. This member must be a multiple of 4.

### -field fOddPages

If <b>TRUE</b>, only the odd-numbered pages in the page-set indicated by <b>rgPages</b> are to be printed.

### -field fEvenPages

If <b>TRUE</b>, only the even-numbered pages in the page-set indicated by <b>rgPages</b> are to be printed.

### -field cPageRange

The number of page-range pairs specified in <b>rgPages</b>.

### -field rgPages

Pointer to an array of <a href="/windows/desktop/api/docobj/ns-docobj-pagerange">PAGERANGE</a> structures specifying the pages to be printed. One or more page ranges can be specified, so long as the number of page ranges is the value of <b>cPageRange</b>. The page ranges must be sorted in ascending order and must be non-overlapping.

## -see-also

<a href="/windows/desktop/api/docobj/ns-docobj-pagerange">PAGERANGE</a>
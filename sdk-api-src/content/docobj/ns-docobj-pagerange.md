---
UID: NS:docobj.tagPAGERANGE
title: PAGERANGE (docobj.h)
description: Specifies a range of pages.
helpviewer_keywords: ["PAGERANGE","PAGERANGE structure [COM]","_ctrl_PAGERANGE","com.pagerange","docobj/PAGERANGE"]
old-location: com\pagerange.htm
tech.root: com
ms.assetid: b37d57e6-1634-4676-9f31-e3db2835983f
ms.date: 12/05/2018
ms.keywords: PAGERANGE, PAGERANGE structure [COM], _ctrl_PAGERANGE, com.pagerange, docobj/PAGERANGE
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
req.typenames: PAGERANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPAGERANGE
 - docobj/tagPAGERANGE
 - PAGERANGE
 - docobj/PAGERANGE
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
 - PAGERANGE
---

# PAGERANGE structure


## -description

Specifies a range of pages.

## -struct-fields

### -field nFromPage

The first page of the range. This member can have any page number as a value. If this value is greater than the value specified in <b>nToPage</b>, the document will be printed in reverse page order.

### -field nToPage

The last page of the range. A special value, <b>PAGESET_TOLASTPAGE</b>, indicates that all the remaining pages should be printed. This member can have any page number as a value. If this value is less than the value specified in <b>nFromPage</b>, the document will be printed in reverse page order.

## -see-also

<a href="/windows/desktop/api/docobj/ns-docobj-pageset">PAGESET</a>
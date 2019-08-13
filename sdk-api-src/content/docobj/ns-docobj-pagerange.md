---
UID: NS:docobj.tagPAGERANGE
title: PAGERANGE (docobj.h)
author: windows-sdk-content
description: Specifies a range of pages.
old-location: com\pagerange.htm
tech.root: com
ms.assetid: b37d57e6-1634-4676-9f31-e3db2835983f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PAGERANGE, PAGERANGE structure [COM], _ctrl_PAGERANGE, com.pagerange, docobj/PAGERANGE
ms.topic: struct
f1_keywords: 
 - "docobj/PAGERANGE"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Docobj.h
api_name:
 - PAGERANGE
product: Windows
targetos: Windows
req.typenames: PAGERANGE
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/docobj/ns-docobj-pageset">PAGESET</a>
 

 


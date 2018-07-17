---
UID: NS:docobj.tagPAGERANGE
title: tagPAGERANGE
author: windows-sdk-content
description: Specifies a range of pages.
old-location: com\pagerange.htm
old-project: com
ms.assetid: b37d57e6-1634-4676-9f31-e3db2835983f
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: PAGERANGE, PAGERANGE structure [COM], _ctrl_PAGERANGE, com.pagerange, docobj/PAGERANGE, tagPAGERANGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: docobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DocObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PAGERANGE
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
req.lib: 
req.dll: 
req.irql: 
---

# tagPAGERANGE structure


## -description


Specifies a range of pages.


## -struct-fields




### -field nFromPage

The first page of the range. This member can have any page number as a value. If this value is greater than the value specified in <b>nToPage</b>, the document will be printed in reverse page order.


### -field nToPage

The last page of the range. A special value, <b>PAGESET_TOLASTPAGE</b>, indicates that all the remaining pages should be printed. This member can have any page number as a value. If this value is less than the value specified in <b>nFromPage</b>, the document will be printed in reverse page order.


## -see-also




<a href="https://msdn.microsoft.com/9639c743-2509-4611-833b-16d16fce420a">PAGESET</a>
 

 


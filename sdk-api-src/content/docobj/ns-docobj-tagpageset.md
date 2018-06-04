---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# tagPAGESET structure


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

Pointer to an array of <a href="https://msdn.microsoft.com/b37d57e6-1634-4676-9f31-e3db2835983f">PAGERANGE</a> structures specifying the pages to be printed. One or more page ranges can be specified, so long as the number of page ranges is the value of <b>cPageRange</b>. The page ranges must be sorted in ascending order and must be non-overlapping. 


## -see-also




<a href="https://msdn.microsoft.com/b37d57e6-1634-4676-9f31-e3db2835983f">PAGERANGE</a>
 

 


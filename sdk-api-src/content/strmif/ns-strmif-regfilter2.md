---
UID: NS:strmif.REGFILTER2
title: REGFILTER2
author: windows-sdk-content
description: The REGFILTER2 structure contains information for registering a filter.
old-location: dshow\regfilter2.htm
tech.root: DirectShow
ms.assetid: 651b94e6-b343-4957-9781-768b04c098dd
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: REGFILTER2, REGFILTER2 structure [DirectShow], REGFILTER2Structure, dshow.regfilter2, strmif/REGFILTER2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - REGFILTER2
product: Windows
targetos: Windows
req.typenames: REGFILTER2
req.redist: 
---

# REGFILTER2 structure


## -description



The <code>REGFILTER2</code> structure contains information for registering a filter.




## -struct-fields




### -field dwVersion

Filter registration format. If the value is 1, the union contains the first unnamed structure. If the value is 2, the union contains the second unnamed structure.


### -field dwMerit

Filter merit. Filters with higher merit are enumerated first. See <a href="https://msdn.microsoft.com/9e026675-e0a9-4c82-9b57-ab0e7d9592ea">Merit</a>.


### -field cPins

Number of pins. (Defined only if <b>dwVersion</b> is 1.)


### -field rgPins

Pointer to an array of <a href="https://msdn.microsoft.com/1da033e1-24c3-46e0-becf-025966e6238f">REGFILTERPINS</a> structures, of size <b>cPins</b>. (Defined only if <b>dwVersion</b> is 1.)


### -field cPins2

Number of pins. (Defined only if <b>dwVersion</b> is 2.)


### -field rgPins2

Pointer to an array of <a href="https://msdn.microsoft.com/a78327f1-a0aa-4e25-b6f8-cf45b92191fa">REGFILTERPINS2</a> structures, of size <b>cPins2</b>. (Defined only if <b>dwVersion</b> is 2.)


## -remarks



This structure is passed to the <a href="https://msdn.microsoft.com/773e527e-2174-4f74-a822-549cfe2927a3">IFilterMapper2::RegisterFilter</a> method.

If you need to register pin mediums or pin categories, set <b>dwVersion</b> to 2 and use the <a href="https://msdn.microsoft.com/a78327f1-a0aa-4e25-b6f8-cf45b92191fa">REGFILTERPINS2</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 


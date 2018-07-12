---
UID: NS:strmif.REGFILTERPINS2
title: REGFILTERPINS2
author: windows-sdk-content
description: The REGFILTERPINS2 structure contains information for registering a filter through the IFilterMapper2 interface.
old-location: dshow\regfilterpins2.htm
old-project: DirectShow
ms.assetid: a78327f1-a0aa-4e25-b6f8-cf45b92191fa
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: REGFILTERPINS2, REGFILTERPINS2 structure [DirectShow], REGFILTERPINS2Structure, dshow.regfilterpins2, strmif/REGFILTERPINS2
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
tech.root: 
req.typenames: REGFILTERPINS2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - REGFILTERPINS2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# REGFILTERPINS2 structure


## -description



The <code>REGFILTERPINS2</code> structure contains information for registering a filter through the <a href="https://msdn.microsoft.com/6a3db838-cee3-4a9f-a924-fb55931acc83">IFilterMapper2</a> interface.




## -struct-fields




### -field dwFlags

Bitwise combination of zero or more <a href="https://msdn.microsoft.com/85d9f9b6-229f-41ea-87bb-097af591c2d2">REG_PINFLAG</a> flags.


### -field cInstances

Number of instances of this pin.


### -field nMediaTypes

Number of media types supported by this pin.


### -field lpMediaType

Pointer to an array of <a href="https://msdn.microsoft.com/aa31f856-4151-420d-a69d-34ef3a105130">REGPINTYPES</a> structures, of size nMediaTypes.


### -field nMediums

Number of mediums. Can be zero.


### -field lpMedium

Pointer to an array of <a href="https://msdn.microsoft.com/ed5614fe-bfeb-4ddf-a626-b14080f45b33">REGPINMEDIUM</a> structures, of size nMediums.


### -field clsPinCategory

Optional pin category, from the <a href="https://msdn.microsoft.com/0c01bd51-353d-4f48-b33c-796f740915e2">Pin Property Set</a>.


## -remarks



If you use this structure, set the <b>dwVersion</b> member of the <a href="https://msdn.microsoft.com/651b94e6-b343-4957-9781-768b04c098dd">REGFILTER2</a> structure to 2.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 


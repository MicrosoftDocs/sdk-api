---
UID: NS:wingdi.tagMETARECORD
title: tagMETARECORD
author: windows-sdk-content
description: The METARECORD structure contains a Windows-format metafile record.
old-location: gdi\metarecord.htm
tech.root: gdi
ms.assetid: 7c5d6e97-dff1-4c80-a7d3-082413dca469
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPMETARECORD, *PMETARECORD, METARECORD, METARECORD structure [Windows GDI], PMETARECORD, PMETARECORD structure pointer [Windows GDI], _win32_METARECORD_str, gdi.metarecord, tagMETARECORD, wingdi/METARECORD, wingdi/PMETARECORD"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
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
 - Wingdi.h
api_name:
 - METARECORD
product: Windows
targetos: Windows
req.typenames: METARECORD, *PMETARECORD, *LPMETARECORD
req.redist: 
---

# tagMETARECORD structure


## -description



The <b>METARECORD</b> structure contains a Windows-format metafile record.




## -struct-fields




### -field rdSize

The size, in words, of the record.


### -field rdFunction

The function number.


### -field rdParm

An array of words containing the function parameters, in reverse of the order they are passed to the function.


## -see-also




<a href="https://msdn.microsoft.com/3ad5be24-9558-442e-8c77-dd6a7d33c208">METAHEADER</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


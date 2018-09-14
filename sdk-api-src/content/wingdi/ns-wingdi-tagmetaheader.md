---
UID: NS:wingdi.tagMETAHEADER
title: tagMETAHEADER
author: windows-sdk-content
description: The METAHEADER structure contains information about a Windows-format metafile.
old-location: gdi\metaheader.htm
tech.root: gdi
ms.assetid: 3ad5be24-9558-442e-8c77-dd6a7d33c208
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*LPMETAHEADER, *PMETAHEADER, METAHEADER, METAHEADER structure [Windows GDI], PMETAHEADER, PMETAHEADER structure pointer [Windows GDI], _win32_METAHEADER_str, gdi.metaheader, tagMETAHEADER, wingdi/METAHEADER, wingdi/PMETAHEADER"
ms.prod: windows
ms.technology: windows-sdk
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
 - METAHEADER
product: Windows
targetos: Windows
req.typenames: METAHEADER, *PMETAHEADER, *LPMETAHEADER
req.redist: 
---

# tagMETAHEADER structure


## -description



The <b>METAHEADER</b> structure contains information about a Windows-format metafile.




## -struct-fields




### -field mtType

Specifies whether the metafile is in memory or recorded in a disk file. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>1</td>
<td>Metafile is in memory.</td>
</tr>
<tr>
<td>2</td>
<td>Metafile is in a disk file.</td>
</tr>
</table>
 


### -field mtHeaderSize

The size, in words, of the metafile header.


### -field mtVersion

The system version number. The version number for metafiles that support device-independent bitmaps (DIBs) is 0x0300. Otherwise, the version number is 0x0100.


### -field mtSize

The size, in words, of the file.


### -field mtNoObjects

The maximum number of objects that exist in the metafile at the same time.


### -field mtMaxRecord

The size, in words, of the largest record in the metafile.


### -field mtNoParameters

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/7c5d6e97-dff1-4c80-a7d3-082413dca469">METARECORD</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


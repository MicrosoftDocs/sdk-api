---
UID: NS:wingdi.tagENHMETARECORD
title: tagENHMETARECORD
author: windows-sdk-content
description: The ENHMETARECORD structure contains data that describes a graphics device interface (GDI) function used to create part of a picture in an enhanced-format metafile.
old-location: gdi\enhmetarecord.htm
tech.root: gdi
ms.assetid: efe49094-fe61-40e1-873e-3302c595717e
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*LPENHMETARECORD, *PENHMETARECORD, ENHMETARECORD, ENHMETARECORD structure [Windows GDI], PENHMETARECORD, PENHMETARECORD structure pointer [Windows GDI], _win32_ENHMETARECORD_str, gdi.enhmetarecord, tagENHMETARECORD, wingdi/ENHMETARECORD, wingdi/PENHMETARECORD"
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
 - ENHMETARECORD
product: Windows
targetos: Windows
req.typenames: ENHMETARECORD, *PENHMETARECORD, *LPENHMETARECORD
req.redist: 
---

# tagENHMETARECORD structure


## -description



The <b>ENHMETARECORD</b> structure contains data that describes a graphics device interface (GDI) function used to create part of a picture in an enhanced-format metafile.




## -struct-fields




### -field iType

The record type.


### -field nSize

The size of the record, in bytes.


### -field dParm

An array of parameters passed to the GDI function identified by the record.


## -see-also




<a href="https://msdn.microsoft.com/8e5f9a51-a995-48be-b936-1766fccb603a">ENHMETAHEADER</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


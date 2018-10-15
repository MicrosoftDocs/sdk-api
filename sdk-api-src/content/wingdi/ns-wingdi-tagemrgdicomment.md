---
UID: NS:wingdi.tagEMRGDICOMMENT
title: tagEMRGDICOMMENT
author: windows-sdk-content
description: The EMRGDICOMMENT structure contains application-specific data.
old-location: gdi\emrgdicomment.htm
tech.root: gdi
ms.assetid: aac18154-bd50-45a4-a1ba-390b59525fa9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PEMRGDICOMMENT, EMRGDICOMMENT, EMRGDICOMMENT structure [Windows GDI], PEMRGDICOMMENT, PEMRGDICOMMENT structure pointer [Windows GDI], _win32_EMRGDICOMMENT_str, gdi.emrgdicomment, tagEMRGDICOMMENT, wingdi/EMRGDICOMMENT, wingdi/PEMRGDICOMMENT"
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
 - EMRGDICOMMENT
product: Windows
targetos: Windows
req.typenames: EMRGDICOMMENT, *PEMRGDICOMMENT
req.redist: 
---

# tagEMRGDICOMMENT structure


## -description



The <b>EMRGDICOMMENT</b> structure contains application-specific data. This enhanced metafile record is only meaningful to applications that know the format of the data and how to utilize it. This record is ignored by graphics device interface (GDI) during playback of the enhanced metafile.




## -struct-fields




### -field emr

The base structure for all record types.


### -field cbData

Size of data buffer, in bytes.


### -field Data

 




#### - Data[1]

Application-specific data.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


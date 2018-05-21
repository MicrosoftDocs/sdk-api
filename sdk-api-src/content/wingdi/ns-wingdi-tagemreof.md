---
UID: NS:wingdi.tagEMREOF
title: tagEMREOF
author: windows-driver-content
description: The EMREOF structure contains data for the enhanced metafile record that indicates the end of the metafile.
old-location: gdi\emreof.htm
old-project: gdi
ms.assetid: 99a3f97e-cb43-49b3-9972-23f9911b2cd0
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*PEMREOF, EMREOF, EMREOF structure [Windows GDI], PEMREOF, PEMREOF structure pointer [Windows GDI], _win32_EMREOF_str, gdi.emreof, tagEMREOF, wingdi/EMREOF, wingdi/PEMREOF"
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
req.typenames: EMREOF, *PEMREOF
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMREOF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMREOF structure


## -description



The <b>EMREOF</b> structure contains data for the enhanced metafile record that indicates the end of the metafile.




## -struct-fields




### -field emr

The base structure for all record types.


### -field nPalEntries

The number of palette entries.


### -field offPalEntries

The offset, in bytes, to an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures.


### -field nSizeLast

The same size as the <b>nSize</b> member of the <a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a> structure. This member must be the last double word of the record. If palette entries exist, they precede this member.


## -see-also




<a href="https://msdn.microsoft.com/06582047-b64b-44ec-ae27-1f8ed7c56b97">EMR</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>
 

 


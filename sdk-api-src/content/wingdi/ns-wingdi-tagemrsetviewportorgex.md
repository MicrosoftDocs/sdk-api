---
UID: NS:wingdi.tagEMRSETVIEWPORTORGEX
title: tagEMRSETVIEWPORTORGEX
author: windows-driver-content
description: The EMRSETVIEWPORTORGEX, EMRSETWINDOWORGEX, and EMRSETBRUSHORGEX structures contain members for the SetViewportOrgEx, SetWindowOrgEx, and SetBrushOrgEx enhanced metafile records.
old-location: gdi\emrsetviewportorgex__emrsetwindoworgex__emrsetbrushorgex.htm
old-project: gdi
ms.assetid: df80b89a-67b2-4ab3-8ff8-f121f9eb88cd
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: "*PEMRSETBRUSHORGEX, *PEMRSETVIEWPORTORGEX, *PEMRSETWINDOWORGEX, EMRSETBRUSHORGEX, EMRSETBRUSHORGEX structure [Windows GDI], EMRSETVIEWPORTORGEX, EMRSETVIEWPORTORGEX structure [Windows GDI], EMRSETVIEWPORTORGEX,EMRSETWINDOWORGEX,EMRSETBRUSHORGEX, EMRSETVIEWPORTORGEX,EMRSETWINDOWORGEX,EMRSETBRUSHORGEX structure [Windows GDI], EMRSETWINDOWORGEX, EMRSETWINDOWORGEX structure [Windows GDI], PEMRSETBRUSHORGEX, PEMRSETBRUSHORGEX structure pointer [Windows GDI], PEMRSETVIEWPORTORGEX, PEMRSETVIEWPORTORGEX structure pointer [Windows GDI], PEMRSETWINDOWORGEX, PEMRSETWINDOWORGEX structure pointer [Windows GDI], _win32_EMRSETVIEWPORTORGEX_str, gdi.emrsetviewportorgex__emrsetwindoworgex__emrsetbrushorgex, tagEMRSETVIEWPORTORGEX, wingdi/EMRSETBRUSHORGEX, wingdi/EMRSETVIEWPORTORGEX,EMRSETWINDOWORGEX,EMRSETBRUSHORGEX, wingdi/EMRSETWINDOWORGEX, wingdi/PEMRSETBRUSHORGEX, wingdi/PEMRSETVIEWPORTORGEX, wingdi/PEMRSETWINDOWORGEX"
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
req.typenames: EMRSETVIEWPORTORGEX, *PEMRSETVIEWPORTORGEX, EMRSETWINDOWORGEX, *PEMRSETWINDOWORGEX, EMRSETBRUSHORGEX, *PEMRSETBRUSHORGEX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRSETVIEWPORTORGEX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRSETVIEWPORTORGEX structure


## -description



The <b>EMRSETVIEWPORTORGEX, </b><b>EMRSETWINDOWORGEX, </b> and <b>EMRSETBRUSHORGEX</b> structures contain members for the <b>SetViewportOrgEx</b>, <b>SetWindowOrgEx</b>, and <b>SetBrushOrgEx</b> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field ptlOrigin

Coordinates of the origin. For <b>EMRSETVIEWPORTORGEX</b> and <b>EMRSETBRUSHORGEX</b>, this is in device units. For <b>EMRSETWINDOWORGEX</b>, this is in logical units.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a>



<a href="https://msdn.microsoft.com/d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4">SetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/75409b5a-c003-49f2-aceb-a28330b92b0a">SetWindowOrgEx</a>
 

 


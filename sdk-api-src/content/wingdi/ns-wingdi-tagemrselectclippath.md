---
UID: NS:wingdi.tagEMRSELECTCLIPPATH
title: tagEMRSELECTCLIPPATH
author: windows-sdk-content
description: Contains parameters for the SelectClipPath, SetBkMode, SetMapMode, SetPolyFillMode, SetROP2, SetStretchBltMode, SetTextAlign, SetICMMode , and SetLayout enhanced metafile records.
old-location: gdi\enhanced_metafile_records_with_one_parameter.htm
tech.root: gdi
ms.assetid: cae5eb68-169e-4439-9141-af93c8ff5ec6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "#if(WINVER >= 0x0500) EMRSETLAYOUT, #if(WINVER >= 0x0500) EMRSETLAYOUT structure [Windows GDI], *PEMRSELECTCLIPPATH, *PEMRSETBKMODE, *PEMRSETICMMODE, *PEMRSETLAYOUT, *PEMRSETMAPMODE, *PEMRSETPOLYFILLMODE, *PEMRSETROP2, *PEMRSETSTRETCHBLTMODE, *PEMRSETTEXTALIGN, EMRSELECTCLIPPATH, EMRSELECTCLIPPATH structure [Windows GDI], EMRSETBKMODE, EMRSETBKMODE structure [Windows GDI], EMRSETICMMODE, EMRSETICMMODE structure [Windows GDI], EMRSETLAYOUT, EMRSETMAPMODE, EMRSETMAPMODE structure [Windows GDI], EMRSETPOLYFILLMODE, EMRSETPOLYFILLMODE structure [Windows GDI], EMRSETROP2, EMRSETROP2 structure [Windows GDI], EMRSETSTRETCHBLTMODE, EMRSETSTRETCHBLTMODE structure [Windows GDI], EMRSETTEXTALIGN, EMRSETTEXTALIGN structure [Windows GDI], Enhanced Metafile Records with One Parameter, Enhanced Metafile Records with One Parameter structure [Windows GDI], PEMRSELECTCLIPPATH, PEMRSELECTCLIPPATH structure pointer [Windows GDI], PEMRSETBKMODE, PEMRSETBKMODE structure pointer [Windows GDI], PEMRSETICMMODE, PEMRSETICMMODE structure pointer [Windows GDI], PEMRSETLAYOUT #endif / WINVER >= 0x0500 /, PEMRSETLAYOUT #endif / WINVER >= 0x0500 / structure pointer [Windows GDI], PEMRSETMAPMODE, PEMRSETMAPMODE structure pointer [Windows GDI], PEMRSETPOLYFILLMODE, PEMRSETPOLYFILLMODE structure pointer [Windows GDI], PEMRSETROP2, PEMRSETROP2 structure pointer [Windows GDI], PEMRSETSTRETCHBLTMODE, PEMRSETSTRETCHBLTMODE structure pointer [Windows GDI], PEMRSETTEXTALIGN, PEMRSETTEXTALIGN structure pointer [Windows GDI], _win32_Enhanced_Metafile_Records_with_One_Parameter_str, gdi.enhanced_metafile_records_with_one_parameter, tagEMRSELECTCLIPPATH, wingdi/#if(WINVER >= 0x0500) EMRSETLAYOUT, wingdi/EMRSETBKMODE, wingdi/EMRSETICMMODE, wingdi/EMRSETMAPMODE, wingdi/EMRSETPOLYFILLMODE, wingdi/EMRSETROP2, wingdi/EMRSETSTRETCHBLTMODE, wingdi/EMRSETTEXTALIGN, wingdi/Enhanced Metafile Records with One Parameter, wingdi/PEMRSELECTCLIPPATH, wingdi/PEMRSETBKMODE, wingdi/PEMRSETICMMODE, wingdi/PEMRSETLAYOUT #endif / WINVER >= 0x0500 /, wingdi/PEMRSETMAPMODE, wingdi/PEMRSETPOLYFILLMODE, wingdi/PEMRSETROP2, wingdi/PEMRSETSTRETCHBLTMODE, wingdi/PEMRSETTEXTALIGN"
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
 - EMRSELECTCLIPPATH
product: Windows
targetos: Windows
req.typenames: EMRSELECTCLIPPATH, *PEMRSELECTCLIPPATH, EMRSETBKMODE, *PEMRSETBKMODE, EMRSETMAPMODE, *PEMRSETMAPMODE, EMRSETLAYOUT, *PEMRSETLAYOUT, EMRSETPOLYFILLMODE, *PEMRSETPOLYFILLMODE, EMRSETROP2, *PEMRSETROP2, EMRSETSTRETCHBLTMODE, *PEMRSETSTRETCHBLTMODE, EMRSETICMMODE, *PEMRSETICMMODE, EMRSETTEXTALIGN, *PEMRSETTEXTALIGN
req.redist: 
---

# tagEMRSELECTCLIPPATH structure


## -description



Contains parameters for the <a href="https://msdn.microsoft.com/c5102e1b-ba33-4cce-a4e5-93cf10c1c0bb">SelectClipPath</a>, <a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a>, <a href="https://msdn.microsoft.com/a4d6a63a-6d2d-4bd9-9e71-4cd1b5f145a4">SetMapMode</a>, <a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a>, <a href="https://msdn.microsoft.com/a462a03d-e2c8-403e-aab4-ae03fb96f06f">SetROP2</a>, <a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>, <a href="https://msdn.microsoft.com/422868c5-14c9-4374-9cc5-b7bf91ab9eb4">SetTextAlign</a>, <a href="https://msdn.microsoft.com/40d70c1f-c580-43c4-b44b-6c9388e138fb">SetICMMode</a> , and <a href="https://msdn.microsoft.com/81c6dccd-cfb1-486f-8c25-f46ba7c3ff8d">SetLayout</a> enhanced metafile records.




## -struct-fields




### -field emr

The base structure for all record types.


### -field iMode

A value and meaning that varies depending on the function contained in the enhanced metafile record. For a description of this member, see the documentation of the functions contained in this record.


## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/c5102e1b-ba33-4cce-a4e5-93cf10c1c0bb">SelectClipPath</a>



<a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a>



<a href="https://msdn.microsoft.com/40d70c1f-c580-43c4-b44b-6c9388e138fb">SetICMMode</a>



<a href="https://msdn.microsoft.com/a4d6a63a-6d2d-4bd9-9e71-4cd1b5f145a4">SetMapMode</a>



<a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a>



<a href="https://msdn.microsoft.com/a462a03d-e2c8-403e-aab4-ae03fb96f06f">SetROP2</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>



<a href="https://msdn.microsoft.com/422868c5-14c9-4374-9cc5-b7bf91ab9eb4">SetTextAlign</a>
 

 


---
UID: NS:wingdi.tagEMRSETCOLORSPACE
title: EMRSETCOLORSPACE
author: windows-sdk-content
description: The EMRSETCOLORSPACE, EMRSELECTCOLORSPACE, and EMRDELETECOLORSPACE structures contain members for the SetColorSpace and DeleteColorSpace enhanced metafile records.
old-location: gdi\emrsetcolorspace__emrselectcolorspace__emrdeletecolorspace.htm
tech.root: gdi
ms.assetid: c661b3cc-6b41-4157-acb4-f9083ab73851
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEMRDELETECOLORSPACE, *PEMRSELECTCOLORSPACE, *PEMRSETCOLORSPACE, EMRDELETECOLORSPACE, EMRDELETECOLORSPACE structure [Windows GDI], EMRSELECTCOLORSPACE, EMRSELECTCOLORSPACE structure [Windows GDI], EMRSETCOLORSPACE, EMRSETCOLORSPACE structure [Windows GDI], EMRSETCOLORSPACE,EMRSELECTCOLORSPACE,EMRDELETECOLORSPACE, EMRSETCOLORSPACE,EMRSELECTCOLORSPACE,EMRDELETECOLORSPACE structure [Windows GDI], PEMRDELETECOLORSPACE, PEMRDELETECOLORSPACE structure pointer [Windows GDI], PEMRSELECTCOLORSPACE, PEMRSELECTCOLORSPACE structure pointer [Windows GDI], PEMRSETCOLORSPACE, PEMRSETCOLORSPACE structure pointer [Windows GDI], _win32_EMRSETCOLORSPACE_str, gdi.emrsetcolorspace__emrselectcolorspace__emrdeletecolorspace, wingdi/EMRDELETECOLORSPACE, wingdi/EMRSELECTCOLORSPACE, wingdi/EMRSETCOLORSPACE,EMRSELECTCOLORSPACE,EMRDELETECOLORSPACE, wingdi/PEMRDELETECOLORSPACE, wingdi/PEMRSELECTCOLORSPACE, wingdi/PEMRSETCOLORSPACE"
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
 - EMRSETCOLORSPACE
product: Windows
targetos: Windows
req.typenames: EMRSETCOLORSPACE, *PEMRSETCOLORSPACE, EMRSELECTCOLORSPACE, *PEMRSELECTCOLORSPACE, EMRDELETECOLORSPACE, *PEMRDELETECOLORSPACE
req.redist: 
---

# EMRSETCOLORSPACE structure


## -description



The <b>EMRSETCOLORSPACE</b>, <b>EMRSELECTCOLORSPACE</b>, and <b>EMRDELETECOLORSPACE</b> structures contain members for the <b>SetColorSpace</b> and <b>DeleteColorSpace</b> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field ihCS

Color space handle index.


## -remarks



There is no function that generates an enhanced metafile record with the <b>EMRSELECTCOLORSPACE</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


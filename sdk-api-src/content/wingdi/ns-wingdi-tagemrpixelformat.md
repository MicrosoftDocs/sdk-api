---
UID: NS:wingdi.tagEMRPIXELFORMAT
title: tagEMRPIXELFORMAT
author: windows-sdk-content
description: The EMRPIXELFORMAT structure contains the members for the SetPixelFormat enhanced metafile record. The pixel format information in ENHMETAHEADER refers to this structure.
old-location: gdi\emrpixelformat.htm
tech.root: gdi
ms.assetid: 3dd2ef54-af00-4d7e-b33f-c7c5160ae4f1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PEMRPIXELFORMAT, EMRPIXELFORMAT, EMRPIXELFORMAT structure [Windows GDI], PEMRPIXELFORMAT, PEMRPIXELFORMAT structure pointer [Windows GDI], _win32_EMRPIXELFORMAT_str, gdi.emrpixelformat, tagEMRPIXELFORMAT, wingdi/EMRPIXELFORMAT, wingdi/PEMRPIXELFORMAT"
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
 - EMRPIXELFORMAT
product: Windows
targetos: Windows
req.typenames: EMRPIXELFORMAT, *PEMRPIXELFORMAT
req.redist: 
---

# tagEMRPIXELFORMAT structure


## -description



The <b>EMRPIXELFORMAT</b> structure contains the members for the <a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a> enhanced metafile record. The pixel format information in <a href="https://msdn.microsoft.com/8e5f9a51-a995-48be-b936-1766fccb603a">ENHMETAHEADER</a> refers to this structure.




## -struct-fields




### -field emr

The base structure for all record types.


### -field pfd

A 
            <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure, which describes the pixel format.


## -see-also




<a href="https://msdn.microsoft.com/8e5f9a51-a995-48be-b936-1766fccb603a">ENHMETAHEADER</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a>
 

 


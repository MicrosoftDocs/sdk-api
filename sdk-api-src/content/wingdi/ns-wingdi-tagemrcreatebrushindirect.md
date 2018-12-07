---
UID: NS:wingdi.tagEMRCREATEBRUSHINDIRECT
title: tagEMRCREATEBRUSHINDIRECT
author: windows-sdk-content
description: The EMRCREATEBRUSHINDIRECT structure contains members for the CreateBrushIndirect enhanced metafile record.
old-location: gdi\emrcreatebrushindirect.htm
tech.root: gdi
ms.assetid: fd87d52a-1227-48ba-8b7e-a8fd007c9d01
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PEMRCREATEBRUSHINDIRECT, EMRCREATEBRUSHINDIRECT, EMRCREATEBRUSHINDIRECT structure [Windows GDI], PEMRCREATEBRUSHINDIRECT, PEMRCREATEBRUSHINDIRECT structure pointer [Windows GDI], _win32_EMRCREATEBRUSHINDIRECT_str, gdi.emrcreatebrushindirect, tagEMRCREATEBRUSHINDIRECT, wingdi/EMRCREATEBRUSHINDIRECT, wingdi/PEMRCREATEBRUSHINDIRECT"
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
 - EMRCREATEBRUSHINDIRECT
product: Windows
targetos: Windows
req.typenames: EMRCREATEBRUSHINDIRECT, *PEMRCREATEBRUSHINDIRECT
req.redist: 
---

# tagEMRCREATEBRUSHINDIRECT structure


## -description



The <b>EMRCREATEBRUSHINDIRECT</b> structure contains members for the <a href="https://msdn.microsoft.com/75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7">CreateBrushIndirect</a> enhanced metafile record.




## -struct-fields




### -field emr

The base structure for all record types.


### -field ihBrush

Index of brush in handle table.


### -field lb

A <a href="https://msdn.microsoft.com/8e2053a9-d7b6-4bf7-b915-4c3871a46b37">LOGBRUSH32</a> structure containing information about the brush. The <b>lbStyle</b> member must be either the BS_SOLID, BS_HOLLOW, BS_NULL, or BS_HATCHED value.

Note, that if your code is used on both 32-bit and 64-bit platforms, you must use the <a href="https://msdn.microsoft.com/8e2053a9-d7b6-4bf7-b915-4c3871a46b37">LOGBRUSH32</a> structure. This maintains compatibility between the platforms when you record the metafile on one platform and use it on the other platform. If your code remains on one platform, it is sufficient to use <a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>.


## -see-also




<a href="https://msdn.microsoft.com/75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7">CreateBrushIndirect</a>



<a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>



<a href="https://msdn.microsoft.com/8e2053a9-d7b6-4bf7-b915-4c3871a46b37">LOGBRUSH32</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


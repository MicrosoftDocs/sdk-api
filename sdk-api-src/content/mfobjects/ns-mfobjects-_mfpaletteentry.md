---
UID: NS:mfobjects._MFPaletteEntry
title: "_MFPaletteEntry"
author: windows-driver-content
description: Contains one palette entry in a color table.
old-location: mf\mfpaletteentry.htm
old-project: medfound
ms.assetid: 72e45756-b1aa-4db0-a6e7-2e6ea97211b4
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: 72e45756-b1aa-4db0-a6e7-2e6ea97211b4, MFPaletteEntry, MFPaletteEntry union [Media Foundation], _MFPaletteEntry, mf.mfpaletteentry, mfobjects/MFPaletteEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFPaletteEntry
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfobjects.h
api_name:
-	MFPaletteEntry
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFPaletteEntry structure


## -description


Contains one palette entry in a color table.


## -struct-fields




### -field ARGB


<a href="https://msdn.microsoft.com/ce7ac174-9f00-42a4-9b48-ed86b406d83e">MFARGB</a> structure that contains an RGB color.


### -field AYCbCr


<a href="https://msdn.microsoft.com/9784b561-3b87-4df9-a434-55e12f97b05a">MFAYUVSample</a> structure that contains a Y'Cb'Cr' color.


## -remarks



This union can be used to represent both RGB palettes and Y'Cb'Cr' palettes. The video format that defines the palette determines which union member should be used.




## -see-also




<a href="https://msdn.microsoft.com/03d97d26-714d-4aec-bb92-0772f09b7cca">Media Foundation Unions</a>
 

 


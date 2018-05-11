---
UID: NF:winddi.STROBJ_bEnum
title: STROBJ_bEnum function
author: windows-driver-content
description: The STROBJ_bEnum function enumerates glyph identities and positions.
old-location: display\strobj_benum.htm
old-project: display
ms.assetid: 82cb12ff-2baa-4291-849c-dab9d01fa39b
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: STROBJ_bEnum, STROBJ_bEnum function [Display Devices], display.strobj_benum, gdifncs_2925a0a5-f797-41a5-b5b1-d87d60d44905.xml, winddi/STROBJ_bEnum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	STROBJ_bEnum
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# STROBJ_bEnum function


## -description


The <b>STROBJ_bEnum</b> function enumerates glyph identities and positions.


## -parameters




### -param pstro

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure containing the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a> information.


### -param pc

Pointer to the count, returned by GDI, of GLYPHPOS structures.


### -param ppgpos

Pointer to the array in which GDI writes the GLYPHPOS structures.


## -returns



The return value is <b>TRUE</b> if more glyphs remain to be enumerated, or <b>FALSE</b> if the enumeration is complete. The return value is DDI_ERROR if the glyphs cannot be enumerated, and an error code is logged.




## -remarks



A driver should download only the glyph handles if it caches fonts itself.

The information returned depends on the driver's return value for <a href="https://msdn.microsoft.com/library/windows/hardware/ff556230">DrvGetGlyphMode</a>. 

Bitmaps or outlines can also be obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structures.

Printer drivers should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff569740">STROBJ_bEnumPositionsOnly</a> instead of <b>STROBJ_bEnum</b> if printer hardware provides internal rendering of TrueType fonts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556230">DrvGetGlyphMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565982">FONTOBJ_cGetGlyphs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566824">GLYPHPOS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569740">STROBJ_bEnumPositionsOnly</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569745">STROBJ_vEnumStart</a>
 

 


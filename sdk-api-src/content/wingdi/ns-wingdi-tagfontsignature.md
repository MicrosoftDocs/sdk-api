---
UID: NS:wingdi.tagFONTSIGNATURE
title: tagFONTSIGNATURE
author: windows-driver-content
description: Contains information identifying the code pages and Unicode subranges for which a given font provides glyphs.
old-location: intl\fontsignature.htm
old-project: Intl
ms.assetid: 5331da53-7e3d-46e9-a922-da04fedc8382
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*LPFONTSIGNATURE, *PFONTSIGNATURE, FONTSIGNATURE, FONTSIGNATURE structure [Internationalization for Windows Applications], PFONTSIGNATURE, PFONTSIGNATURE structure pointer [Internationalization for Windows Applications], _win32_FONTSIGNATURE_str, intl.fontsignature, tagFONTSIGNATURE, wingdi/FONTSIGNATURE, wingdi/PFONTSIGNATURE"
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
req.typenames: FONTSIGNATURE, *PFONTSIGNATURE, *LPFONTSIGNATURE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	FONTSIGNATURE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagFONTSIGNATURE structure


## -description



Contains information identifying the code pages and Unicode subranges for which a given font provides glyphs.




## -struct-fields




### -field fsUsb

A 128-bit Unicode subset bitfield (USB) identifying up to 126 Unicode subranges. Each bit, except the two most significant bits, represents a single subrange. The most significant bit is always 1 and identifies the bitfield as a font signature; the second most significant bit is reserved and must be 0. Unicode subranges are numbered in accordance with the ISO 10646 standard. For more information, see <a href="https://msdn.microsoft.com/f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d">Unicode Subset Bitfields</a>.


### -field fsCsb

A 64-bit, code-page bitfield (CPB) that identifies a specific character set or code page. Code pages are in the lower 32 bits of this bitfield. The high 32 are used for non-Windows code pages. For more information, see <a href="https://msdn.microsoft.com/830b1a88-cb0c-4719-b857-4cc2cd67dd5d">Code Page Bitfields</a>.


## -remarks



GDI relies on Windows code pages fitting within a 32-bit value. Furthermore, the highest 2 bits within this value are reserved for GDI internal use and may not be assigned to code pages.




## -see-also




<a href="https://msdn.microsoft.com/54510d73-f2a2-4176-8080-cdf855e99217">LOCALESIGNATURE</a>



<a href="https://msdn.microsoft.com/0c8120dd-3270-4343-8b0c-b91ff555f276">Unicode and Character Set Structures</a>
 

 


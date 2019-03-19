---
UID: NS:wingdi.tagLOCALESIGNATURE
title: LOCALESIGNATURE (wingdi.h)
author: windows-sdk-content
description: Contains extended font signature information, including two code page bitfields (CPBs) that define the default and supported character sets and code pages. This structure is typically used to represent the relationships between font coverage and locales.
old-location: intl\localesignature.htm
tech.root: Intl
ms.assetid: 54510d73-f2a2-4176-8080-cdf855e99217
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPLOCALESIGNATURE, *PLOCALESIGNATURE, LOCALESIGNATURE, LOCALESIGNATURE structure [Internationalization for Windows Applications], PLOCALESIGNATURE, PLOCALESIGNATURE structure pointer [Internationalization for Windows Applications], _win32_LOCALESIGNATURE_str, intl.localesignature, wingdi/LOCALESIGNATURE, wingdi/PLOCALESIGNATURE"
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
 - LOCALESIGNATURE
product: Windows
targetos: Windows
req.typenames: LOCALESIGNATURE, *PLOCALESIGNATURE, *LPLOCALESIGNATURE
req.redist: 
---

# LOCALESIGNATURE structure


## -description



Contains extended font signature information, including two code page bitfields (CPBs) that define the default and supported character sets and code pages. This structure is typically used to represent the relationships between font coverage and locales.




## -struct-fields




### -field lsUsb

A 128-bit Unicode subset bitfield (USB) identifying up to 122 Unicode subranges. Each bit, except the five most significant bits, represents a single subrange. The most significant bit is always 1; the second most significant is reserved and must be 0. Unicode subsets are numbered in accordance with the <a href="https://msdn.microsoft.com/0d67481a-79ff-448c-b77c-a55bf935a22a">OpenType font specification</a>. For a list of possible bitfield values, see <a href="https://msdn.microsoft.com/f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d">Unicode Subset Bitfields</a>.


### -field lsCsbDefault

A code page bitfield that indicates the default OEM and ANSI code pages for a locale. The code pages can be identified by separate bits or a single bit representing a common ANSI and OEM code page. For a list of possible bitfield values, see <a href="https://msdn.microsoft.com/830b1a88-cb0c-4719-b857-4cc2cd67dd5d">Code Page Bitfields</a>.


### -field lsCsbSupported

A code page bitfield that indicates all the code pages in which the locale can be supported. For a list of possible bitfield values, see <a href="https://msdn.microsoft.com/830b1a88-cb0c-4719-b857-4cc2cd67dd5d">Code Page Bitfields</a>.


## -see-also




<a href="https://msdn.microsoft.com/5331da53-7e3d-46e9-a922-da04fedc8382">FONTSIGNATURE</a>



<a href="https://msdn.microsoft.com/0c8120dd-3270-4343-8b0c-b91ff555f276">Unicode and Character Set Structures</a>
 

 


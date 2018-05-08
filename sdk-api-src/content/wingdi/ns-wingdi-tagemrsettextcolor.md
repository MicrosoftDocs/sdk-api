---
UID: NS:wingdi.tagEMRSETTEXTCOLOR
title: tagEMRSETTEXTCOLOR
author: windows-driver-content
description: The EMRSETBKCOLOR and EMRSETTEXTCOLOR structures contain members for the SetBkColor and SetTextColor enhanced metafile records.
old-location: gdi\emrsetbkcolor__emrsettextcolor.htm
old-project: gdi
ms.assetid: 9916fc79-cac0-4c46-8fa5-aeca3b7f2cf0
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*PEMRSETBKCOLOR, *PEMRSETTEXTCOLOR, EMRSETBKCOLOR, EMRSETBKCOLOR structure [Windows GDI], EMRSETBKCOLOR,EMRSETTEXTCOLOR, EMRSETBKCOLOR,EMRSETTEXTCOLOR structure [Windows GDI], EMRSETTEXTCOLOR, EMRSETTEXTCOLOR structure [Windows GDI], PEMRSETBKCOLOR, PEMRSETBKCOLOR structure pointer [Windows GDI], PEMRSETTEXTCOLOR, PEMRSETTEXTCOLOR structure pointer [Windows GDI], _win32_EMRSETBKCOLOR_str, gdi.emrsetbkcolor__emrsettextcolor, tagEMRSETTEXTCOLOR, wingdi/EMRSETBKCOLOR,EMRSETTEXTCOLOR, wingdi/EMRSETTEXTCOLOR, wingdi/PEMRSETBKCOLOR, wingdi/PEMRSETTEXTCOLOR"
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
req.typenames: EMRSETBKCOLOR, *PEMRSETBKCOLOR, EMRSETTEXTCOLOR, *PEMRSETTEXTCOLOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	EMRSETBKCOLOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagEMRSETTEXTCOLOR structure


## -description



The <b>EMRSETBKCOLOR</b> and <b>EMRSETTEXTCOLOR</b> structures contain members for the <b>SetBkColor</b> and <b>SetTextColor</b> enhanced metafile records.




## -struct-fields




### -field emr

Base structure for all record types.


### -field crColor

Color value. To make a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/6a509ed5-cea3-4318-ad17-9d20425a6e80">Metafile Structures</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 


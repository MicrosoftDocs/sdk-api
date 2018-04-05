---
UID: NE:dwrite.DWRITE_NUMBER_SUBSTITUTION_METHOD
title: DWRITE_NUMBER_SUBSTITUTION_METHOD
author: windows-driver-content
description: Specifies how to apply number substitution on digits and related punctuation.
old-location: directwrite\dwrite_number_substitution_method.htm
old-project: DirectWrite
ms.assetid: 9702007f-ab08-4ad2-9fac-6482e17161ca
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DWRITE_NUMBER_SUBSTITUTION_METHOD, DWRITE_NUMBER_SUBSTITUTION_METHOD enumeration [Direct Write], DWRITE_NUMBER_SUBSTITUTION_METHOD_CONTEXTUAL, DWRITE_NUMBER_SUBSTITUTION_METHOD_FROM_CULTURE, DWRITE_NUMBER_SUBSTITUTION_METHOD_NATIONAL, DWRITE_NUMBER_SUBSTITUTION_METHOD_NONE, DWRITE_NUMBER_SUBSTITUTION_METHOD_TRADITIONAL, directwrite.dwrite_number_substitution_method, dwrite/DWRITE_NUMBER_SUBSTITUTION_METHOD, dwrite/DWRITE_NUMBER_SUBSTITUTION_METHOD_CONTEXTUAL, dwrite/DWRITE_NUMBER_SUBSTITUTION_METHOD_FROM_CULTURE, dwrite/DWRITE_NUMBER_SUBSTITUTION_METHOD_NATIONAL, dwrite/DWRITE_NUMBER_SUBSTITUTION_METHOD_NONE, dwrite/DWRITE_NUMBER_SUBSTITUTION_METHOD_TRADITIONAL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dwrite.h
api_name:
-	DWRITE_NUMBER_SUBSTITUTION_METHOD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DWRITE_NUMBER_SUBSTITUTION_METHOD enumeration


## -description


Specifies how to apply number substitution on digits and related punctuation.


## -enum-fields




### -field DWRITE_NUMBER_SUBSTITUTION_METHOD_FROM_CULTURE

Specifies that the substitution method should be determined based on the LOCALE_IDIGITSUBSTITUTION value of the specified text culture.


### -field DWRITE_NUMBER_SUBSTITUTION_METHOD_CONTEXTUAL

If the culture is Arabic or Persian, specifies that the number shapes depend on the context. Either traditional or nominal number shapes are used, depending on the nearest preceding strong character or (if there is none) the reading direction of the paragraph.


### -field DWRITE_NUMBER_SUBSTITUTION_METHOD_NONE

Specifies that code points 0x30-0x39 are always rendered as nominal numeral shapes (ones of the European number), that is, no substitution is performed.


### -field DWRITE_NUMBER_SUBSTITUTION_METHOD_NATIONAL

Specifies that numbers are rendered using the national number shapes as specified by the LOCALE_SNATIVEDIGITS value of the specified text culture.


### -field DWRITE_NUMBER_SUBSTITUTION_METHOD_TRADITIONAL

Specifies that numbers are rendered using the traditional shapes for the specified culture. For most cultures, this is the same as NativeNational. However, NativeNational results in Latin numbers for some Arabic cultures, whereasDWRITE_NUMBER_SUBSTITUTION_METHOD_TRADITIONAL results in arabic numbers for all Arabic cultures.


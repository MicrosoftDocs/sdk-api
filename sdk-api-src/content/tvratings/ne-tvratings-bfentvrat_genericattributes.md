---
UID: NE:tvratings.BfEnTvRat_GenericAttributes
title: BfEnTvRat_GenericAttributes
author: windows-sdk-content
description: This topic applies to Windows XP Service Pack 1 or later.
old-location: mstv\bfentvrat_genericattributes.htm
tech.root: MSTV
ms.assetid: eb7f56c4-1d48-43f9-a691-c08aee3cd537
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BfAttrNone, BfEnTvRat_GenericAttributes, BfEnTvRat_GenericAttributes enumeration [Microsoft TV Technologies], BfIsAttr_1, BfIsAttr_2, BfIsAttr_3, BfIsAttr_4, BfIsAttr_5, BfIsAttr_6, BfIsAttr_7, BfIsBlocked, BfValidAttrSubmask, mstv.bfentvrat_genericattributes, tvratings/BfAttrNone, tvratings/BfEnTvRat_GenericAttributes, tvratings/BfIsAttr_1, tvratings/BfIsAttr_2, tvratings/BfIsAttr_3, tvratings/BfIsAttr_4, tvratings/BfIsAttr_5, tvratings/BfIsAttr_6, tvratings/BfIsAttr_7, tvratings/BfIsBlocked, tvratings/BfValidAttrSubmask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: tvratings.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tvratings.h
api_name:
 - BfEnTvRat_GenericAttributes
product: Windows
targetos: Windows
req.typenames: BfEnTvRat_GenericAttributes
req.redist: 
---

# BfEnTvRat_GenericAttributes enumeration


## -description



This topic applies to Windows XP Service Pack 1 or later.
        



The <b>BfEnTvRat_GenericAttributes</b> enumeration type specifies additional content-rating attributes that can be used for any rating system, including custom rating systems.


## -enum-fields




### -field BfAttrNone

No restrictions are in place.


### -field BfIsBlocked

Block all content, regardless of other flags.


### -field BfIsAttr_1

Generic attribute 1.


### -field BfIsAttr_2

Generic attribute 2.


### -field BfIsAttr_3

Generic attribute 3.


### -field BfIsAttr_4

Generic attribute 4.


### -field BfIsAttr_5

Generic attribute 5.


### -field BfIsAttr_6

Generic attribute 6.


### -field BfIsAttr_7

Generic attribute 7.


### -field BfValidAttrSubmask

A bitmask of all valid attribute bits.


## -remarks



The <b>BfIsBlocked</b> flag specifies that a program should be blocked regardless of the type of content. Flags in the range <b>BfIsAttr_1</b> to <b>BfIsAttr_7</b> represent generic content attributes, such as violence or adult language. Content attributes do not apply to every ratings system. For an example of how these generic attributes map to a particular system, see <a href="https://msdn.microsoft.com/3ad1736f-d27f-4aba-ab68-e7aca407d182">BfEnTvRat_Attributes_US_TV</a>.




## -see-also




<a href="https://msdn.microsoft.com/5406cb4b-e843-463c-95e0-0da7e4152978">TV Ratings Enumerations</a>
 

 


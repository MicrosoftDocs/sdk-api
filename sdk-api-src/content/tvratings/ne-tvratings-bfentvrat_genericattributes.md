---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 


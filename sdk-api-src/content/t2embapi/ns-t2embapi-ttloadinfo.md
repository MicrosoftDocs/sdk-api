---
UID: NS:t2embapi.TTLOADINFO
title: TTLOADINFO
author: windows-driver-content
description: The TTLOADINFO structure contains the URL from which the embedded font object has been obtained.
old-location: gdi\ttloadinfo.htm
old-project: gdi
ms.assetid: 7a4beae7-cd30-47e3-b310-d0a79c3c8c36
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: TTLOADINFO, TTLOADINFO structure [Windows GDI], _win32_TTLOADINFO, gdi.ttloadinfo, t2embapi/TTLOADINFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: t2embapi.h
req.include-header: 
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
req.typenames: TTLOADINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	T2embapi.h
api_name:
-	TTLOADINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TTLOADINFO structure


## -description



The <b>TTLOADINFO</b> structure contains the URL from which the embedded font object has been obtained.




## -struct-fields




### -field usStructSize

Size, in bytes, of this structure. The client should set this value to <b>sizeof</b>(TTLOADINFO).


### -field usRefStrSize

Size, in wide characters, of <i>pusRefStr</i>, including the terminating null character.


### -field pusRefStr

Pointer to the string containing the current URL.


## -see-also




<a href="https://msdn.microsoft.com/7e1828bf-c9ed-4120-b91f-b4eb45191e48">TTEMBEDINFO</a>



<a href="https://msdn.microsoft.com/85181d86-bc18-4948-bc7d-65c2d71efefb">TTLoadEmbeddedFont</a>
 

 


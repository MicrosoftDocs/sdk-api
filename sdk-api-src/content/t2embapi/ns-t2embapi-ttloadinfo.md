---
UID: NS:t2embapi.__unnamed_struct_0
title: TTLOADINFO (t2embapi.h)
author: windows-sdk-content
description: The TTLOADINFO structure contains the URL from which the embedded font object has been obtained.
old-location: gdi\ttloadinfo.htm
tech.root: gdi
ms.assetid: 7a4beae7-cd30-47e3-b310-d0a79c3c8c36
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TTLOADINFO, TTLOADINFO structure [Windows GDI], _win32_TTLOADINFO, gdi.ttloadinfo, t2embapi/TTLOADINFO
ms.topic: struct
f1_keywords: 
 - "t2embapi/TTLOADINFO"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - T2embapi.h
api_name:
 - TTLOADINFO
targetos: Windows
req.typenames: TTLOADINFO
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/ns-t2embapi-ttembedinfo">TTEMBEDINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/t2embapi/nf-t2embapi-ttloadembeddedfont">TTLoadEmbeddedFont</a>
 

 


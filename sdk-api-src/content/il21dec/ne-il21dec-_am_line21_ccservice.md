---
UID: NE:il21dec._AM_LINE21_CCSERVICE
title: "_AM_LINE21_CCSERVICE"
author: windows-sdk-content
description: Indicates the closed captioning service.
old-location: dshow\am_line21_ccservice.htm
old-project: DirectShow
ms.assetid: dd2b618f-ffbf-4d48-bbe8-6d237a0f54e8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: "*PAM_LINE21_CCSERVICE, AM_L21_CCSERVICE_Caption1, AM_L21_CCSERVICE_Caption2, AM_L21_CCSERVICE_None, AM_L21_CCSERVICE_Text1, AM_L21_CCSERVICE_Text2, AM_L21_CCSERVICE_XDS, AM_LINE21_CCSERVICE, AM_LINE21_CCSERVICE , AM_LINE21_CCSERVICE enumeration [DirectShow], AM_LINE21_CCSERVICEEnumeration, PAM_LINE21_CCSERVICE, PAM_LINE21_CCSERVICE enumeration pointer [DirectShow], _AM_LINE21_CCSERVICE, dshow.am_line21_ccservice, il21dec/AM_L21_CCSERVICE_Caption1, il21dec/AM_L21_CCSERVICE_Caption2, il21dec/AM_L21_CCSERVICE_None, il21dec/AM_L21_CCSERVICE_Text1, il21dec/AM_L21_CCSERVICE_Text2, il21dec/AM_L21_CCSERVICE_XDS, il21dec/AM_LINE21_CCSERVICE, il21dec/PAM_LINE21_CCSERVICE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: il21dec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AM_LINE21_CCSERVICE, *PAM_LINE21_CCSERVICE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - il21dec.h
api_name:
 - AM_LINE21_CCSERVICE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _AM_LINE21_CCSERVICE enumeration


## -description



Indicates the closed captioning service.




## -enum-fields




### -field AM_L21_CCSERVICE_None


            No current service.
          


### -field AM_L21_CCSERVICE_Caption1


            CC1 (caption channel).
          


### -field AM_L21_CCSERVICE_Caption2


            CC2 (caption channel).
          


### -field AM_L21_CCSERVICE_Text1


            T1 (text channel).
          


### -field AM_L21_CCSERVICE_Text2


            T2 (text channel)
          


### -field AM_L21_CCSERVICE_XDS


            Extended Data Services (XDS or EDS).
          


### -field AM_L21_CCSERVICE_DefChannel


### -field AM_L21_CCSERVICE_Invalid




## -remarks



The Line 21 decoder supports CC1 and CC2 only.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/bfd1c33d-27e0-4923-9c80-5d1bedb4fd25">IAMLine21Decoder::GetCurrentService</a>



<a href="https://msdn.microsoft.com/2f1945c3-644d-4e72-b2b7-a7e068b59d96">IAMLine21Decoder::SetCurrentService</a>
 

 


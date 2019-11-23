---
UID: NF:gdiplusheaders.CustomLineCap.SetStrokeCaps
title: CustomLineCap::SetStrokeCaps (gdiplusheaders.h)

description: The CustomLineCap::SetStrokeCaps method sets the LineCap objects used to start and end lines within the GraphicsPath object that defines this CustomLineCap object.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetStrokeCaps_startCap_endCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setstrokecaps.htm

ms.date: 12/05/2018
ms.keywords: CustomLineCap class [GDI+],SetStrokeCaps method, CustomLineCap.SetStrokeCaps, CustomLineCap::SetStrokeCaps, SetStrokeCaps, SetStrokeCaps method [GDI+], SetStrokeCaps method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetStrokeCaps_startCap_endCap_, gdiplus._gdiplus_CLASS_CustomLineCap_SetStrokeCaps_startCap_endCap_
ms.topic: method
f1_keywords: 
 - "gdiplusheaders/CustomLineCap.SetStrokeCaps"
dev_langs:
 - c++
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - CustomLineCap.SetStrokeCaps
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# CustomLineCap::SetStrokeCaps


## -description


The <b>CustomLineCap::SetStrokeCaps</b> method sets the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> objects used to start and end lines within the <a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object that defines this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a> object.


## -parameters




### -param startCap [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that specifies the line cap that will be used for the start of the line to be drawn. 


### -param endCap [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a> enumeration that specifies the line cap that will be used for the end of the line to be drawn. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 


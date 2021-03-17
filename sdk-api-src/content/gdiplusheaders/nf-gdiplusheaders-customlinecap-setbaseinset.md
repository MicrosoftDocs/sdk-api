---
UID: NF:gdiplusheaders.CustomLineCap.SetBaseInset
title: CustomLineCap::SetBaseInset (gdiplusheaders.h)
description: The CustomLineCap::SetBaseInset method sets the base inset value of this custom line cap. This is the distance between the end of a line and the base cap.
helpviewer_keywords: ["CustomLineCap class [GDI+]","SetBaseInset method","CustomLineCap.SetBaseInset","CustomLineCap::SetBaseInset","SetBaseInset","SetBaseInset method [GDI+]","SetBaseInset method [GDI+]","CustomLineCap class","_gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_","gdiplus._gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_"]
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setbaseinset.htm
ms.date: 12/05/2018
ms.keywords: CustomLineCap class [GDI+],SetBaseInset method, CustomLineCap.SetBaseInset, CustomLineCap::SetBaseInset, SetBaseInset, SetBaseInset method [GDI+], SetBaseInset method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_, gdiplus._gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - CustomLineCap::SetBaseInset
 - gdiplusheaders/CustomLineCap::SetBaseInset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - CustomLineCap.SetBaseInset
---

# CustomLineCap::SetBaseInset


## -description

The <b>CustomLineCap::SetBaseInset</b> method sets the base inset value of this custom line cap. This is the distance between the end of a line and the base cap.

## -parameters

### -param inset [in]

Type: <b>REAL</b>

Real number that specifies the distance, in units, from the base cap to the start of the line. If this value is greater than the length of the line, the behavior of this method is undefined.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.
                

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-linecap">LineCap</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
---
UID: NF:gdiplusheaders.Region.FromHRGN
title: Region::FromHRGN (gdiplusheaders.h)
description: The Region::FromHRGN method creates a Windows GDI+Region object from a Windows Graphics Device Interface (GDI)  region.
helpviewer_keywords: ["FromHRGN","FromHRGN method [GDI+]","FromHRGN method [GDI+]","Region class","Region class [GDI+]","FromHRGN method","Region.FromHRGN","Region::FromHRGN","_gdiplus_CLASS_Region_FromHRGN_hRgn_","gdiplus._gdiplus_CLASS_Region_FromHRGN_hRgn_"]
old-location: gdiplus\_gdiplus_CLASS_Region_FromHRGN_hRgn_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\fromhrgn.htm
ms.date: 12/05/2018
ms.keywords: FromHRGN, FromHRGN method [GDI+], FromHRGN method [GDI+],Region class, Region class [GDI+],FromHRGN method, Region.FromHRGN, Region::FromHRGN, _gdiplus_CLASS_Region_FromHRGN_hRgn_, gdiplus._gdiplus_CLASS_Region_FromHRGN_hRgn_
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
 - Region::FromHRGN
 - gdiplusheaders/Region::FromHRGN
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
 - Region.FromHRGN
---

# Region::FromHRGN


## -description

The <b>Region::FromHRGN</b> method creates a Windows GDI+<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object from a Windows Graphics Device Interface (GDI)  region.

## -parameters

### -param hRgn [in]

Type: <b>HRGN</b>

Handle to an existing GDI region.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object.
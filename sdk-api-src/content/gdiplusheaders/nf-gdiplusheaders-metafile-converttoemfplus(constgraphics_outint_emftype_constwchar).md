---
UID: NF:gdiplusheaders.Metafile.ConvertToEmfPlus(constGraphics,INT,EmfType,constWCHAR)
title: Metafile::ConvertToEmfPlus (gdiplusheaders.h)
description: The Metafile::ConvertToEmfPlus method converts this Metafile object to the EMF+ format. (overload 1/3)
helpviewer_keywords: ["ConvertToEmfPlus","ConvertToEmfPlus method [GDI+]","ConvertToEmfPlus method [GDI+]","Metafile class","Metafile class [GDI+]","ConvertToEmfPlus method","Metafile.ConvertToEmfPlus","Metafile::ConvertToEmfPlus","_gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_","gdiplus._gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\metafileconverttoemfplusmethods\converttoemfplus_graphicsrefgraphics_bool.htm
ms.date: 12/05/2018
ms.keywords: ConvertToEmfPlus, ConvertToEmfPlus method [GDI+], ConvertToEmfPlus method [GDI+],Metafile class, Metafile class [GDI+],ConvertToEmfPlus method, Metafile.ConvertToEmfPlus, Metafile::ConvertToEmfPlus, _gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_, gdiplus._gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Metafile::ConvertToEmfPlus
 - gdiplusheaders/Metafile::ConvertToEmfPlus
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
 - Metafile.ConvertToEmfPlus
---

# Metafile::ConvertToEmfPlus


## -description

The <b>Metafile::ConvertToEmfPlus</b> method converts this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a> object to the EMF+ format.

## -parameters

### -param refGraphics [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object whose state (settings for antialiasing, interpolation, and the like) is applied to the records stored in the converted metafile.

### -param conversionFailureFlag [out]

Type: <b>BOOL*</b>

Optional. Pointer to a <b>BOOL</b> that receives <b>TRUE</b> if all the metafile records were converted successfully; <b>FALSE</b> otherwise. Pass <b>NULL</b> if you do not want to receive this information. The default value is <b>NULL</b>.

### -param emfType [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a></b>

Optional. Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-emftype">EmfType</a> enumeration that specifies whether the converted file has the <b>EmfTypeEmfPlusOnly</b> format or the <b>EmfTypeEmfPlusDual</b> format. Do not pass <b>EmfTypeEmfOnly</b>. The default value is <b>EmfTypeEmfPlusOnly</b>.

### -param description [in]

Type: <b>const WCHAR*</b>

Optional. Pointer to a null-terminated wide-character string that is stored in the header of the converted metafile. The default value is <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns OK, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

This method replaces the records originally in the <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a> object with the converted records. To retain a copy of the original <b>Metafile</b> object, call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-clone">Clone</a> method.

If you set the <i>emfType</i> parameter to <b>EmfTypeEmfPlusDual</b>, the converted metafile contains an Enhanced Metafile (EMF) representation and an EMF+ representation. The EMF representation is the original set of EMF records rather than EMF records converted back from the newly created EMF+ records.

It is possible for the return value to be <b>Ok</b> and the value returned in <i>conversionSuccess</i> to be <b>FALSE</b>. Sometimes the overall conversion is considered to be successful even if a few individual records failed to convert with complete accuracy. For example, the original metafile might have records or operations that are not supported by Windows GDI+ (or EMF+), in which case those records or operations are emulated.

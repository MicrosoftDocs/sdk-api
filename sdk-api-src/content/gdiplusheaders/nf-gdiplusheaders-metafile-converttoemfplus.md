---
UID: NF:gdiplusheaders.Metafile.ConvertToEmfPlus
title: Metafile::ConvertToEmfPlus
author: windows-driver-content
description: The Metafile::ConvertToEmfPlus method converts this Metafile object to the EMF+ format.
old-location: gdiplus\_gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\metafileconverttoemfplusmethods\converttoemfplus_graphicsrefgraphics_bool.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ConvertToEmfPlus, ConvertToEmfPlus method [GDI+], ConvertToEmfPlus method [GDI+],Metafile class, Metafile class [GDI+],ConvertToEmfPlus method, Metafile.ConvertToEmfPlus, Metafile::ConvertToEmfPlus, _gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_, gdiplus._gdiplus_CLASS_Metafile_ConvertToEmfPlus_Graphics_refGraphics_BOOL_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Metafile.ConvertToEmfPlus
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Metafile::ConvertToEmfPlus


## -description


The <b>Metafile::ConvertToEmfPlus</b> method converts this <a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object to the EMF+ format.


## -parameters




### -param refGraphics [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object whose state (settings for antialiasing, interpolation, and the like) is applied to the records stored in the converted metafile.


### -param conversionFailureFlag




### -param emfType [in]

Type: <b><a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfType</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfType</a> enumeration that specifies whether the converted file has the <b>EmfTypeEmfPlusOnly</b> format or the <b>EmfTypeEmfPlusDual</b> format. Do not pass <b>EmfTypeEmfOnly</b>. The default value is <b>EmfTypeEmfPlusOnly</b>.


### -param description [in]

Type: <b>const WCHAR*</b>

Optional. Pointer to a null-terminated wide-character string that is stored in the header of the converted metafile. The default value is <b>NULL</b>.


#### - conversionSuccess [out]

Type: <b>BOOL*</b>

Optional. Pointer to a <b>BOOL</b> that receives <b>TRUE</b> if all the metafile records were converted successfully; <b>FALSE</b> otherwise. Pass <b>NULL</b> if you do not want to receive this information. The default value is <b>NULL</b>.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns OK, which is an element of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



This method replaces the records originally in the <a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object with the converted records. To retain a copy of the original <b>Metafile</b> object, call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a> method.

If you set the <i>emfType</i> parameter to <b>EmfTypeEmfPlusDual</b>, the converted metafile contains an Enhanced Metafile (EMF) representation and an EMF+ representation. The EMF representation is the original set of EMF records rather than EMF records converted back from the newly created EMF+ records.

It is possible for the return value to be <b>Ok</b> and the value returned in <i>conversionSuccess</i> to be <b>FALSE</b>. Sometimes the overall conversion is considered to be successful even if a few individual records failed to convert with complete accuracy. For example, the original metafile might have records or operations that are not supported by Windows GDI+ (or EMF+), in which case those records or operations are emulated.




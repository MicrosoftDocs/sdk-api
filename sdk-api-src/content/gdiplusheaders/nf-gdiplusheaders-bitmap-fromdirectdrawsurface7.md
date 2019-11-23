---
UID: NF:gdiplusheaders.Bitmap.FromDirectDrawSurface7
title: Bitmap::FromDirectDrawSurface7 (gdiplusheaders.h)

description: The Bitmap::FromDirectDrawSurface7 method creates a Bitmap object based on a DirectDraw surface. The Bitmap object maintains a reference to the DirectDraw surface until the Bitmap object is deleted.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromDirectDrawSurface7_surface_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromdirectdrawsurface7.htm

ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],FromDirectDrawSurface7 method, Bitmap.FromDirectDrawSurface7, Bitmap::FromDirectDrawSurface7, FromDirectDrawSurface7, FromDirectDrawSurface7 method [GDI+], FromDirectDrawSurface7 method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromDirectDrawSurface7_surface_, gdiplus._gdiplus_CLASS_Bitmap_FromDirectDrawSurface7_surface_
ms.topic: method
f1_keywords: 
 - "gdiplusheaders/Bitmap.FromDirectDrawSurface7"
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
 - Bitmap.FromDirectDrawSurface7
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Bitmap::FromDirectDrawSurface7


## -description


The <b>Bitmap::FromDirectDrawSurface7</b> method creates a 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on a DirectDraw surface. The 
			<b>Bitmap</b> object maintains a reference to the DirectDraw surface until the 
			<b>Bitmap</b> object is deleted.


## -parameters




### -param surface [in]

Type: <b>IDirectDrawSurface7*</b>

Pointer to an 
					<b>IDirectDraw7</b> COM interface. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>
 

 


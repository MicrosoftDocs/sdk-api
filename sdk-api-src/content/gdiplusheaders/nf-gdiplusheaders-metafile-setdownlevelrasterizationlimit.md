---
UID: NF:gdiplusheaders.Metafile.SetDownLevelRasterizationLimit
title: Metafile::SetDownLevelRasterizationLimit
author: windows-sdk-content
description: Sets the resolution for certain brush bitmaps that are stored in this metafile.
old-location: gdiplus\_gdiplus_CLASS_Metafile_SetDownLevelRasterizationLimit_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafileclass\metafilemethods\setdownlevelrasterizationlimit.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Metafile class [GDI+],SetDownLevelRasterizationLimit method, Metafile.SetDownLevelRasterizationLimit, Metafile::SetDownLevelRasterizationLimit, SetDownLevelRasterizationLimit, SetDownLevelRasterizationLimit method [GDI+], SetDownLevelRasterizationLimit method [GDI+],Metafile class, _gdiplus_CLASS_Metafile_SetDownLevelRasterizationLimit_, gdiplus._gdiplus_CLASS_Metafile_SetDownLevelRasterizationLimit_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Metafile.SetDownLevelRasterizationLimit
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Metafile::SetDownLevelRasterizationLimit


## -description


Sets the resolution for certain brush bitmaps that are stored in this metafile.


## -parameters




### -param metafileRasterizationLimitDpi [in]

Type: <b>UINT</b>

Non-negative integer that specifies the resolution in dpi. If you set this parameter equal to 0, the resolution is set to match the resolution of the device context handle that was passed to the <a href="https://msdn.microsoft.com/a9648287-65d9-47d8-b32b-33f74b4fcd07">Metafile</a> constructor. If you set this parameter to a value greater than 0 but less than 10, the resolution is left unchanged.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns OK, which is an element of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 

						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



The purpose of this method is to prevent metafiles from becoming too large as a result of texture and gradient brushes being stored at high resolution. Suppose you construct a <a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object (for recording an <a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfTypeEmfOnly</a> metafile) based on the device context of a printer that has a resolution of 600 dpi. Also suppose you create a path gradient brush or a texture brush based on a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object that has a resolution of 96 dpi. If the bitmap that represents that brush is stored in the metafile with a resolution of 96 dpi, it will require much less space than if it is stored with a resolution of 600 dpi.

The default rasterization limit for metafiles is 96 dpi. So if you do not call this method at all, path gradient brush and texture brush bitmaps are stored with a resolution of 96 dpi.

The rasterization limit has an effect on metafiles of type <a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfTypeEmfOnly</a> and <a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfTypeEmfPlusDual</a>, but it has no effect on metafiles of type <a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfTypeEmfPlusOnly</a>.


#### Examples




			The following example constructs a <a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> object based on the device context of a printer. The code creates a texture brush based on an a BMP file and then records an ellipse filled with that brush. Assume that the printer has a resolution of 600 dpi and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> object has a resolution of 96 dpi.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get a device context for a printer.
HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\printer1"), NULL, NULL); 

// Construct a Metafile object (for recording) based on a 600-DPI printer.
Metafile metafile(L"Metafile.emf", hdcPrint, EmfTypeEmfOnly);
{     
   // Create a texture brush based on a 96-DPI bitmap. 
   Bitmap bitmap(L"Texture.bmp");
   TextureBrush textureBrush(&amp;bitmap);

   // Set the rasterization limit of the metafile to match the DPI of the
   // printer DC, in this case 600. When the bitmap for the texture brush
   // is stored in the metafile, the bitmap will be expanded by a factor of
   // about 6 horizontally and vertically. That will increase the size of 
   // the bitmap by a factor of about 36.
   metafile.SetDownLevelRasterizationLimit(0);

   // Record an ellipse filled with the texture brush.
   Graphics graphics(&amp;metafile);  
   graphics.FillEllipse(&amp;textureBrush, 10, 10, 40, 40);
}

// The preceding code, along with a particular 24 x 23 bitmap,
// produced a 114 kilobyte metafile. Passing 96, instead of 0, to the 
// SetDownLevelRasterizationLimit method produced a 3.5 kilobyte metafile.
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/985c412f-10ba-4ce9-b0e1-89f5b643c22a">EmfType</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/2b3b59a8-5bbb-47f7-854f-907db16e16f2">Metafile::GetDownLevelRasterizationLimit</a>



<a href="https://msdn.microsoft.com/062de6c2-9f82-415d-860e-2d1afd2ac027">Recording Metafiles</a>
 

 


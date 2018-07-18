---
UID: NF:gdiplusheaders.Image.GetBounds
title: Image::GetBounds
author: windows-sdk-content
description: The Image::GetBounds method gets the bounding rectangle for this image.
old-location: gdiplus\_gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getbounds_74srcrect_srcunit.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetBounds, GetBounds method [GDI+], GetBounds method [GDI+],Image class, Image class [GDI+],GetBounds method, Image.GetBounds, Image::GetBounds, _gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_, gdiplus._gdiplus_CLASS_Image_GetBounds_srcRect_srcUnit_
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
 - Image.GetBounds
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::GetBounds


## -description


The <b>Image::GetBounds</b> method gets the bounding rectangle for this image.


## -parameters




### -param srcRect [out]

Type: <b><a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a> object that receives the bounding rectangle. 


### -param srcUnit [out]

Type: <b><a href="https://msdn.microsoft.com/library/ms534405(v=VS.85).aspx">Unit</a>*</b>

Pointer to a variable that receives an element of the <a href="https://msdn.microsoft.com/library/ms534405(v=VS.85).aspx">Unit</a> enumeration that indicates the unit of measure for the bounding rectangle. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



The bounding rectangle for a metafile does not necessarily have (0, 0) as its upper-left corner. The coordinates of the upper-left corner can be negative or positive, depending on the drawing commands that were issued during the recording of the metafile. For example, suppose a metafile consists of a single ellipse that was recorded with the following statement:

<code>DrawEllipse(&amp;pen, 200, 100, 80, 40);</code>

Then the bounding rectangle for the metafile will enclose that one ellipse. The upper-left corner of the bounding rectangle will not be (0, 0); rather, it will be a point near (200, 100).


#### Examples

The following example creates an 
						<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object based on a metafile and then draws the image. Next, the code calls the <b>Image::GetBounds</b> method to get the bounding rectangle for the image. The code makes two attempts to display 75 percent of the image. The first attempt fails because it specifies (0, 0) for the upper-left corner of the source rectangle. The second attempt succeeds because it uses the 
						<b>X</b> and 
						<b>Y</b> data members returned by <b>Image::GetBounds</b> to specify the upper-left corner of the source rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetBounds(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"SampleMetafile2.emf");
   graphics.DrawImage(&amp;image, 0, 0);

   // Get the bounding rectangle for the image (metafile).
   RectF boundsRect;
   Unit unit;
   image.GetBounds(&amp;boundsRect, &amp;unit);

   // Attempt to draw 75 percent of the image.
   // Less than 75 percent of the image will be visible because the
   // upper-left corner of the image's bounding rectangle is not (0, 0).
   RectF dstRect(250.0f, 0.0f, 100.0f, 50.0f);
   graphics.DrawImage(
      &amp;image,
      dstRect,                  // destination rectangle
      0.0f, 0.0f,               // upper-left corner of source rectangle 
      0.75f*boundsRect.Width,   // width of source rectangle
      boundsRect.Height,        // height of source rectangle
      UnitPixel);

   // Draw 75 percent of the image.
   dstRect.Y = 80.0f;
   graphics.DrawImage(
      &amp;image,
      dstRect,                       // destination rectangle
      boundsRect.X, boundsRect.Y,    // upper-left corner of source rectangle
      0.75f*boundsRect.Width,        // width of source rectangle
      boundsRect.Height,             // height of source rectangle
      UnitPixel);
}</pre>
</td>
</tr>
</table></span></div>
The preceding code, along with a particular file, SampleMetafile2.emf, produced the following output. Note that the first attempt (upper-right) to draw 75 percent of the image shows only about 30 percent of the image.


<img alt="Screen shot showing parts of three an ellipses: all of the first one, 30% of the second, and 75% of the third " src="./images/imagegetbounds1.png"/>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/library/ms535380(v=VS.85).aspx">Image::GetHeight</a>



<a href="https://msdn.microsoft.com/library/ms535397(v=VS.85).aspx">Image::GetWidth</a>



<a href="https://msdn.microsoft.com/library/ms536335(v=VS.85).aspx">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/library/ms534405(v=VS.85).aspx">Unit</a>



<a href="https://msdn.microsoft.com/library/ms533815(v=VS.85).aspx">Using Images, Bitmaps, and Metafiles</a>
 

 


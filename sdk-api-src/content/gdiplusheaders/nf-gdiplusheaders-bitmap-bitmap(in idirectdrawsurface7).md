---
UID: NF:gdiplusheaders.Bitmap.Bitmap(IN IDirectDrawSurface7)
title: Bitmap::Bitmap(IN IDirectDrawSurface7)
author: windows-sdk-content
description: This topic lists the constructors of the Bitmap class. For a complete class listing, see Bitmap Class.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_Constructors.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapconstructors.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Bitmap, Bitmap constructors [GDI+], Bitmap.Bitmap, Bitmap.Bitmap(IN IDirectDrawSurface7), Bitmap::Bitmap, Bitmap::Bitmap(IN IDirectDrawSurface7), _gdiplus_CLASS_Bitmap_Constructors, gdiplus._gdiplus_CLASS_Bitmap_Constructors, gdiplusheaders/Bitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - gdiplusheaders.h
api_name:
 - Bitmap.Bitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Bitmap::Bitmap(IN IDirectDrawSurface7)


## -description


<span>This topic lists the constructors of the 
			<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> class. For a complete class listing, see <b>Bitmap Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536318(v=VS.85).aspx">Bitmap(HICON)</a>
</td>
<td align="left" width="63%">
Creates a
			<b> Bitmap</b> object based on an icon.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536316(v=VS.85).aspx">Bitmap(WCHAR*,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536316(v=VS.85).aspx">Bitmap::Bitmap</a> object based on an image file.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536319(v=VS.85).aspx">Bitmap(IStream*,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536319(v=VS.85).aspx">Bitmap::Bitmap</a> object based on an <b>IStream</b> COM interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536314(v=VS.85).aspx">Bitmap(HBITMAP,HPALETTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536314(v=VS.85).aspx">Bitmap::Bitmap</a> object based on a handle to a Windows GDI bitmap and a handle to a GDI palette.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536317(v=VS.85).aspx">Bitmap(HINSTANCE,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536317(v=VS.85).aspx">Bitmap::Bitmap</a> object based on an application or DLL instance handle and the name of a bitmap resource.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536312(v=VS.85).aspx">Bitmap(BITMAPINFO*,VOID*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536312(v=VS.85).aspx">Bitmap::Bitmap</a> object based on a 
			<b>BITMAPINFO</b> structure and an array of pixel data.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536311(v=VS.85).aspx">Bitmap(INT,INT,Graphics*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536311(v=VS.85).aspx">Bitmap::Bitmap</a> object based on a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object, a width, and a height.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536313(v=VS.85).aspx">Bitmap(INT,INT,PixelFormat)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536313(v=VS.85).aspx">Bitmap::Bitmap</a> object of a specified size and pixel format. The pixel data must be provided after the <b>Bitmap::Bitmap</b> object is constructed.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536310(v=VS.85).aspx">Bitmap(IDirectDrawSurface7*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536310(v=VS.85).aspx">Bitmap::Bitmap</a> object based on a DirectDraw surface. The <b>Bitmap::Bitmap</b> object maintains a reference to the DirectDraw surface until the <b>Bitmap::Bitmap</b> object is deleted or goes out of scope.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536315(v=VS.85).aspx">Bitmap(INT,INT,INT,PixelFormat,BYTE*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536315(v=VS.85).aspx">Bitmap::Bitmap</a> object based on an array of bytes along with size and format information.

</td>
</tr>
</table>

## -parameters


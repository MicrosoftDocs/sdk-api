---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# Bitmap::Bitmap(INT,INT,INT,PixelFormat,BYTE)


## -description


<span>This topic lists the constructors of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> class. For a complete class listing, see <b>Bitmap Class</b>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/353b0b2b-26a5-47b9-86b2-7314fb2a5e1a">Bitmap(HICON)</a>
</td>
<td align="left" width="63%">
Creates a
			<b> Bitmap</b> object based on an icon.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d393778-062c-4e4f-b51c-4d24796ba6e1">Bitmap(WCHAR*,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/0d393778-062c-4e4f-b51c-4d24796ba6e1">Bitmap::Bitmap</a> object based on an image file.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59cd896d-96ee-4815-be02-840024fa141a">Bitmap(IStream*,BOOL)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/59cd896d-96ee-4815-be02-840024fa141a">Bitmap::Bitmap</a> object based on an <b>IStream</b> COM interface.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/850b41d7-3302-4c18-8d01-3bccfd5d02f2">Bitmap(HBITMAP,HPALETTE)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/850b41d7-3302-4c18-8d01-3bccfd5d02f2">Bitmap::Bitmap</a> object based on a handle to a Windows GDI bitmap and a handle to a GDI palette.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/134d80cf-78ca-4be3-8d3e-bcd30497f897">Bitmap(HINSTANCE,WCHAR*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/134d80cf-78ca-4be3-8d3e-bcd30497f897">Bitmap::Bitmap</a> object based on an application or DLL instance handle and the name of a bitmap resource.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca4df139-a33d-454b-be1b-06f86df34a97">Bitmap(BITMAPINFO*,VOID*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/ca4df139-a33d-454b-be1b-06f86df34a97">Bitmap::Bitmap</a> object based on a 
			<b>BITMAPINFO</b> structure and an array of pixel data.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0765d650-4bec-4912-abc1-372dcf3ade5d">Bitmap(INT,INT,Graphics*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/0765d650-4bec-4912-abc1-372dcf3ade5d">Bitmap::Bitmap</a> object based on a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object, a width, and a height.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5335aed-efda-4c21-9543-5c8f94fa7551">Bitmap(INT,INT,PixelFormat)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/c5335aed-efda-4c21-9543-5c8f94fa7551">Bitmap::Bitmap</a> object of a specified size and pixel format. The pixel data must be provided after the <b>Bitmap::Bitmap</b> object is constructed.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de341a70-dec3-4211-9107-c88fd0cf638a">Bitmap(IDirectDrawSurface7*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/de341a70-dec3-4211-9107-c88fd0cf638a">Bitmap::Bitmap</a> object based on a DirectDraw surface. The <b>Bitmap::Bitmap</b> object maintains a reference to the DirectDraw surface until the <b>Bitmap::Bitmap</b> object is deleted or goes out of scope.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1350d27-4e5f-4a28-bbfd-4525b015a0a6">Bitmap(INT,INT,INT,PixelFormat,BYTE*)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/f1350d27-4e5f-4a28-bbfd-4525b015a0a6">Bitmap::Bitmap</a> object based on an array of bytes along with size and format information.

</td>
</tr>
</table>

## -parameters


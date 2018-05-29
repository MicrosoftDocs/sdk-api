---
UID: NF:vfw.IGetFrame.SetFormat
title: IGetFrame::SetFormat
author: windows-sdk-content
description: The SetFormat method sets the decompressed image format of the frames being extracted and optionally provides a buffer for the decompression operation.
old-location: multimedia\igetframe_setformat.htm
old-project: Multimedia
ms.assetid: 96a2afa5-af90-47e0-949a-a1498ed7f82e
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IGetFrame interface [Windows Multimedia],SetFormat method, IGetFrame.SetFormat, IGetFrame::SetFormat, SetFormat, SetFormat method [Windows Multimedia], SetFormat method [Windows Multimedia],IGetFrame interface, _win32_IGetFrame_SetFormat, multimedia.igetframe_setformat, vfw/IGetFrame::SetFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vfw32.lib
-	Vfw32.dll
api_name:
-	IGetFrame.SetFormat
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IGetFrame::SetFormat


## -description



The <b>SetFormat</b> method sets the decompressed image format of the frames being extracted and optionally provides a buffer for the decompression operation.




## -parameters




### -param lpbi

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure defining the decompressed image format. You can also specify <b>NULL</b> or the value <code>((LPBITMAPINFOHEADER) 1)</code> for this parameter. <b>NULL</b> causes the decompressor to choose a format that is appropriate for editing (normally a 24-bit image depth format). The value <code>((LPBITMAPINFOHEADER) 1)</code> causes the decompressor to choose a format appropriate for the current display mode.


### -param lpBits

Pointer to a buffer to contain the decompressed image data. Specify <b>NULL</b> to have this method allocate a buffer.


### -param x

The x-coordinate of the destination rectangle within the DIB specified by <i>lpbi</i>. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.


### -param y

The y-coordinate of the destination rectangle within the DIB specified by <i>lpbi</i>. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.


### -param dx

Width of the destination rectangle. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.


### -param dy

Height of the destination rectangle. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.


#### - ps

Pointer to the interface to a stream.


## -returns



Returns <b>NOERROR</b> if successful, <b>E_OUTOFMEMORY</b> if the decompressed image is larger than the buffer size, or <b>E_FAIL</b> otherwise.




## -remarks



The <i>x</i>, <i>y</i>, <i>dx</i>, and <i>dy</i> parameters identify the portion of the bitmap specified by <i>lpbi</i> and <i>lpBits</i> that receives the decompressed image.

For handlers written in C++, <b>SetFormat</b> has the following syntax:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT SetFormat(LPBITMAPINFOHEADER lpbi, LPVOID lpBits, int x, 
    int y, int dx, int dy); 
 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ced6f7d1-5f27-47f4-a912-8c17ea5fa685">Custom File and Stream Handler Interfaces</a>



<a href="https://msdn.microsoft.com/c61e0118-d405-4c1e-9ae8-ed6a145a5d6b">Custom File and Stream Handlers</a>
 

 


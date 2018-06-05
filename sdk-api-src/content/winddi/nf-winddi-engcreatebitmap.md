---
UID: NF:winddi.EngCreateBitmap
title: EngCreateBitmap function
author: windows-sdk-content
description: The EngCreateBitmap function requests that GDI create and manage a bitmap.
old-location: display\engcreatebitmap.htm
old-project: display
ms.assetid: 51da3fbc-bf6e-47a9-8ee8-ebf34c23b66c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngCreateBitmap, EngCreateBitmap function [Display Devices], display.engcreatebitmap, gdifncs_fde5f304-b931-449c-bba5-3a9f3d814687.xml, winddi/EngCreateBitmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngCreateBitmap
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngCreateBitmap function


## -description


The <b>EngCreateBitmap</b> function requests that GDI create and manage a bitmap. 


## -parameters




### -param sizl

Specifies a SIZEL structure whose members contain the width and height, in pixels, of the bitmap to be created. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure.

If <i>pvBits</i> is not <b>NULL</b>, this value should represent all pixels visible on the device, allowing the device to keep <a href="https://msdn.microsoft.com/3f78ce93-03cd-45aa-9861-cdf6d557e6a5">off-screen memory</a>.


### -param lWidth

Specifies the allocation width of the bitmap, which is the number of bytes that must be added to a pointer to move down one scan line.


### -param iFormat [in]

Specifies the format of the bitmap in terms of the number of bits of color information per pixel that are required. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BMF_1BPP

</td>
<td>
Monochrome

</td>
</tr>
<tr>
<td>
BMF_4BPP

</td>
<td>
4 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_8BPP

</td>
<td>
8 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_16BPP

</td>
<td>
16 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_24BPP

</td>
<td>
24 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_32BPP

</td>
<td>
32 bits per pixel

</td>
</tr>
<tr>
<td>
BMF_4RLE

</td>
<td>
4 bits per pixel; run length encoded

</td>
</tr>
<tr>
<td>
BMF_8RLE

</td>
<td>
8 bits per pixel; run length encoded

</td>
</tr>
</table>
 


### -param fl [in]

Is a bitmask that specifies properties about the bitmap to be created. This parameter can be zero, or any combination of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BMF_NOZEROINIT

</td>
<td>
GDI will not zero-initialize the bitmap when allocating it. This flag is checked only when <i>pvBits</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td>
BMF_TOPDOWN

</td>
<td>
The first scan line represents the top of the bitmap. Note that standard-format bitmaps have the first scan line at the bottom by default.

</td>
</tr>
<tr>
<td>
BMF_USERMEM

</td>
<td>
GDI will allocate the memory for the bitmap from user memory. By default, the memory is allocated from the kernel's address space. This flag should be specified only when the bitmap being created will not be used by other processes. User memory cannot be passed to <a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a> by the printer driver.

</td>
</tr>
</table>
 


### -param pvBits [in]

Pointer to the first scan line of the bitmap that is to be created. If this parameter is <b>NULL</b>, GDI allocates the storage space for the pixels of the bitmap. If <i>pvBits</i> is not <b>NULL</b>, it is a pointer to the buffer for the bitmap.


## -returns



If the function completes successfully, the return value is a handle that identifies the created bitmap. Otherwise, the return value is 0. <b>EngCreateBitmap</b> does not log an error code.




## -remarks



Storage for the bitmap can optionally be provided by the driver.

The driver should associate the created bitmap as a surface by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a> before returning from <a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a>.

The bitmap should be deleted by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff564827">EngDeleteSurface</a> when it is no longer needed.

Frame buffer display drivers should use the <i>pvBits</i> parameter, allowing GDI to do most drawing directly to the display.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564178">EngAllocUserMem</a>
 

 


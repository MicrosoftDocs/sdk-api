---
UID: NF:wingdi.GetEnhMetaFileBits
title: GetEnhMetaFileBits function
author: windows-driver-content
description: The GetEnhMetaFileBits function retrieves the contents of the specified enhanced-format metafile and copies them into a buffer.
old-location: gdi\getenhmetafilebits.htm
old-project: gdi
ms.assetid: 2bbfa0da-5b1e-4843-9777-c2e4c5fd3b78
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetEnhMetaFileBits, GetEnhMetaFileBits function [Windows GDI], _win32_GetEnhMetaFileBits, gdi.getenhmetafilebits, wingdi/GetEnhMetaFileBits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Metafile-l1-1-0.dll
-	Ext-MS-Win-GDI-Metafile-l1-1-1.dll
-	ext-ms-win-gdi-metafile-l1-1-2.dll
-	GDI32Full.dll
api_name:
-	GetEnhMetaFileBits
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetEnhMetaFileBits function


## -description


The <b>GetEnhMetaFileBits</b> function retrieves the contents of the specified enhanced-format metafile and copies them into a buffer.


## -parameters




### -param hEMF

TBD


### -param nSize

TBD


### -param lpData

TBD




#### - cbBuffer [in]

The size, in bytes, of the buffer to receive the data.


#### - hemf [in]

A handle to the enhanced metafile.


#### - lpbBuffer [out]

A pointer to a buffer that receives the metafile data. The buffer must be sufficiently large to contain the data. If <i>lpbBuffer</i> is <b>NULL</b>, the function returns the size necessary to hold the data.


## -returns



If the function succeeds and the buffer pointer is <b>NULL</b>, the return value is the size of the enhanced metafile, in bytes.

If the function succeeds and the buffer pointer is a valid pointer, the return value is the number of bytes copied to the buffer.

If the function fails, the return value is zero.




## -remarks



After the enhanced-metafile bits are retrieved, they can be used to create a memory-based metafile by calling the <a href="https://msdn.microsoft.com/0f21ed97-e37f-4b44-a2eb-b8e284b3dc4b">SetEnhMetaFileBits</a> function.

The <b>GetEnhMetaFileBits</b> function does not invalidate the enhanced-metafile handle. The application must call the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function to delete the handle when it is no longer needed.

The metafile contents retrieved by this function are in the enhanced format. To retrieve the metafile contents in the Windows format, use the <a href="https://msdn.microsoft.com/db61ea3a-44d0-4769-acb4-05a982d3f06f">GetWinMetaFileBits</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/db61ea3a-44d0-4769-acb4-05a982d3f06f">GetWinMetaFileBits</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/0f21ed97-e37f-4b44-a2eb-b8e284b3dc4b">SetEnhMetaFileBits</a>
 

 


---
UID: NF:wingdi.CloseEnhMetaFile
title: CloseEnhMetaFile function
author: windows-sdk-content
description: The CloseEnhMetaFile function closes an enhanced-metafile device context and returns a handle that identifies an enhanced-format metafile.
old-location: gdi\closeenhmetafile.htm
old-project: gdi
ms.assetid: 3c4a0d8b-75a5-4729-8c64-476c36d01a90
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CloseEnhMetaFile, CloseEnhMetaFile function [Windows GDI], _win32_CloseEnhMetaFile, gdi.closeenhmetafile, wingdi/CloseEnhMetaFile
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - CloseEnhMetaFile
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CloseEnhMetaFile function


## -description


The <b>CloseEnhMetaFile</b> function closes an enhanced-metafile device context and returns a handle that identifies an enhanced-format metafile.


## -parameters




### -param hdc [in]

Handle to an enhanced-metafile device context.


## -returns



If the function succeeds, the return value is a handle to an enhanced metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



An application can use the enhanced-metafile handle returned by the <b>CloseEnhMetaFile</b> function to perform the following tasks:

<ul>
<li>Display a picture stored in an enhanced metafile</li>
<li>Create copies of the enhanced metafile</li>
<li>Enumerate, edit, or copy individual records in the enhanced metafile</li>
<li>Retrieve an optional description of the metafile contents from the enhanced-metafile header</li>
<li>Retrieve a copy of the enhanced-metafile header</li>
<li>Retrieve a binary copy of the enhanced metafile</li>
<li>Enumerate the colors in the optional palette</li>
<li>Convert an enhanced-format metafile into a Windows-format metafile</li>
</ul>
When the application no longer needs the enhanced metafile handle, it should release the handle by calling the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7c428828-b239-41d4-926c-88caa0aa7214">CopyEnhMetaFile</a>



<a href="https://msdn.microsoft.com/647f83ca-dca3-44af-a594-5f9ba2bd7607">CreateEnhMetaFile</a>



<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>



<a href="https://msdn.microsoft.com/2bbfa0da-5b1e-4843-9777-c2e4c5fd3b78">GetEnhMetaFileBits</a>



<a href="https://msdn.microsoft.com/db61ea3a-44d0-4769-acb4-05a982d3f06f">GetWinMetaFileBits</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>
 

 


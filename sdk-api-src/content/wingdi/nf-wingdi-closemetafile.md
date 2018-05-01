---
UID: NF:wingdi.CloseMetaFile
title: CloseMetaFile function
author: windows-driver-content
description: The CloseMetaFile function closes a metafile device context and returns a handle that identifies a Windows-format metafile.
old-location: gdi\closemetafile.htm
old-project: gdi
ms.assetid: 8e50457a-8ef8-4e71-8c56-38cfb277f57d
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CloseMetaFile, CloseMetaFile function [Windows GDI], _win32_CloseMetaFile, gdi.closemetafile, wingdi/CloseMetaFile
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
-	Ext-MS-Win-GDI-Metafile-l1-1-1.dll
-	ext-ms-win-gdi-metafile-l1-1-2.dll
-	GDI32Full.dll
api_name:
-	CloseMetaFile
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CloseMetaFile function


## -description


The <b>CloseMetaFile</b> function closes a metafile device context and returns a handle that identifies a Windows-format metafile.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/3c4a0d8b-75a5-4729-8c64-476c36d01a90">CloseEnhMetaFile</a>.</div><div> </div>

## -parameters




### -param hdc [in]

Handle to a metafile device context used to create a Windows-format metafile.


## -returns



If the function succeeds, the return value is a handle to a Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



To convert a Windows-format metafile into a new enhanced-format metafile, use the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function.

When an application no longer needs the Windows-format metafile handle, it should delete the handle by calling the <a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3c4a0d8b-75a5-4729-8c64-476c36d01a90">CloseEnhMetaFile</a>



<a href="https://msdn.microsoft.com/e9f97591-697b-47d0-a748-60fda4d5258c">CopyMetaFile</a>



<a href="https://msdn.microsoft.com/81b3baae-f0e6-4b71-a6de-953ad3376dbd">CreateMetaFile</a>



<a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a>



<a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a>



<a href="https://msdn.microsoft.com/6ca6de2e-79cb-4503-a0d7-f616b8e383eb">GetMetaFileBitsEx</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/044894df-dc8a-41b2-8810-e0a1b8bc19d8">PlayMetaFile</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 


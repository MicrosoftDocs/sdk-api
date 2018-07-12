---
UID: NF:wingdi.CopyEnhMetaFileW
title: CopyEnhMetaFileW function
author: windows-sdk-content
description: The CopyEnhMetaFile function copies the contents of an enhanced-format metafile to a specified file.
old-location: gdi\copyenhmetafile.htm
old-project: gdi
ms.assetid: 7c428828-b239-41d4-926c-88caa0aa7214
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CopyEnhMetaFile, CopyEnhMetaFile function [Windows GDI], CopyEnhMetaFileA, CopyEnhMetaFileW, _win32_CopyEnhMetaFile, gdi.copyenhmetafile, wingdi/CopyEnhMetaFile, wingdi/CopyEnhMetaFileA, wingdi/CopyEnhMetaFileW
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
req.unicode-ansi: CopyEnhMetaFileW (Unicode) and CopyEnhMetaFileA (ANSI)
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CopyEnhMetaFile
 - CopyEnhMetaFileA
 - CopyEnhMetaFileW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CopyEnhMetaFileW function


## -description


The <b>CopyEnhMetaFile</b> function copies the contents of an enhanced-format metafile to a specified file.


## -parameters




### -param hEnh

TBD


### -param lpFileName

TBD




#### - hemfSrc [in]

A handle to the enhanced metafile to be copied.


#### - lpszFile [in]

A pointer to the name of the destination file. If this parameter is <b>NULL</b>, the source metafile is copied to memory.


## -returns



If the function succeeds, the return value is a handle to the copy of the enhanced metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Where text arguments must use Unicode characters, use the <b>CopyEnhMetaFile</b> function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

Applications can use metafiles stored in memory for temporary operations.

When the application no longer needs the enhanced-metafile handle, it should delete the handle by calling the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


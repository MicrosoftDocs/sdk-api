---
UID: NF:wingdi.GetEnhMetaFileA
title: GetEnhMetaFileA function
author: windows-driver-content
description: The GetEnhMetaFile function creates a handle that identifies the enhanced-format metafile stored in the specified file.
old-location: gdi\getenhmetafile.htm
old-project: gdi
ms.assetid: bcb9611e-8e4e-4f87-8a1e-dedbe0042821
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetEnhMetaFile, GetEnhMetaFile function [Windows GDI], GetEnhMetaFileA, GetEnhMetaFileW, _win32_GetEnhMetaFile, gdi.getenhmetafile, wingdi/GetEnhMetaFile, wingdi/GetEnhMetaFileA, wingdi/GetEnhMetaFileW
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
req.unicode-ansi: GetEnhMetaFileW (Unicode) and GetEnhMetaFileA (ANSI)
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
-	Gdi32.dll
-	Ext-MS-Win-GDI-Metafile-L1-1-2.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetEnhMetaFile
-	GetEnhMetaFileA
-	GetEnhMetaFileW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetEnhMetaFileA function


## -description


The <b>GetEnhMetaFile</b> function creates a handle that identifies the enhanced-format metafile stored in the specified file.


## -parameters




### -param lpName

TBD




#### - lpszMetaFile [in]

A pointer to a null-terminated string that specifies the name of an enhanced metafile.


## -returns



If the function succeeds, the return value is a handle to the enhanced metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When the application no longer needs an enhanced-metafile handle, it should delete the handle by calling the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function.

A Windows-format metafile must be converted to the enhanced format before it can be processed by the <b>GetEnhMetaFile</b> function. To convert the file, use the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function.

Where text arguments must use Unicode characters, use this function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e4e5ef5c-d5ea-4931-bbec-1635e8f08c91">Opening an Enhanced Metafile and Displaying Its Contents</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/bcb9611e-8e4e-4f87-8a1e-dedbe0042821">GetEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 


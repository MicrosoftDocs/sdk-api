---
UID: NF:wingdi.CopyMetaFileA
title: CopyMetaFileA function
author: windows-sdk-content
description: The CopyMetaFile function copies the content of a Windows-format metafile to the specified file.
old-location: gdi\copymetafile.htm
tech.root: gdi
ms.assetid: e9f97591-697b-47d0-a748-60fda4d5258c
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CopyMetaFile, CopyMetaFile function [Windows GDI], CopyMetaFileA, CopyMetaFileW, _win32_CopyMetaFile, gdi.copymetafile, wingdi/CopyMetaFile, wingdi/CopyMetaFileA, wingdi/CopyMetaFileW
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
req.unicode-ansi: CopyMetaFileW (Unicode) and CopyMetaFileA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
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
 - CopyMetaFile
 - CopyMetaFileA
 - CopyMetaFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CopyMetaFileA function


## -description


The <b>CopyMetaFile</b> function copies the content of a Windows-format metafile to the specified file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/7c428828-b239-41d4-926c-88caa0aa7214">CopyEnhMetaFile</a>.</div><div> </div>

## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - [in]

A handle to the source Windows-format metafile.


#### - lpszFile [in]

A pointer to the name of the destination file. If this parameter is <b>NULL</b>, the source metafile is copied to memory.


## -returns



If the function succeeds, the return value is a handle to the copy of the Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Where text arguments must use Unicode characters, use this function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

When the application no longer needs the Windows-format metafile handle, it should delete the handle by calling the <a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


---
UID: NF:wingdi.SetMetaFileBitsEx
title: SetMetaFileBitsEx function
author: windows-sdk-content
description: The SetMetaFileBitsEx function creates a memory-based Windows-format metafile from the supplied data.
old-location: gdi\setmetafilebitsex.htm
old-project: gdi
ms.assetid: 232eeba9-f579-4b5f-a31a-416aeb56a909
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SetMetaFileBitsEx, SetMetaFileBitsEx function [Windows GDI], _win32_SetMetaFileBitsEx, gdi.setmetafilebitsex, wingdi/SetMetaFileBitsEx
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
-	SetMetaFileBitsEx
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetMetaFileBitsEx function


## -description


The <b>SetMetaFileBitsEx</b> function creates a memory-based Windows-format metafile from the supplied data.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/0f21ed97-e37f-4b44-a2eb-b8e284b3dc4b">SetEnhMetaFileBits</a>.</div><div> </div>

## -parameters




### -param cbBuffer

TBD


### -param lpData [in]

Pointer to a buffer that contains the Windows-format metafile. (It is assumed that the data was obtained by using the <a href="https://msdn.microsoft.com/6ca6de2e-79cb-4503-a0d7-f616b8e383eb">GetMetaFileBitsEx</a> function.)


#### - nSize [in]

Specifies the size, in bytes, of the Windows-format metafile.


## -returns



If the function succeeds, the return value is a handle to a memory-based Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function.

When the application no longer needs the metafile handle returned by <b>SetMetaFileBitsEx</b>, it should delete it by calling the <a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a>



<a href="https://msdn.microsoft.com/6ca6de2e-79cb-4503-a0d7-f616b8e383eb">GetMetaFileBitsEx</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/0f21ed97-e37f-4b44-a2eb-b8e284b3dc4b">SetEnhMetaFileBits</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 


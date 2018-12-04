---
UID: NF:wingdi.SetWinMetaFileBits
title: SetWinMetaFileBits function
author: windows-sdk-content
description: The SetWinMetaFileBits function converts a metafile from the older Windows format to the new enhanced format and stores the new metafile in memory.
old-location: gdi\setwinmetafilebits.htm
tech.root: gdi
ms.assetid: b7170c8a-da5f-4946-9c56-da3cffc84567
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: SetWinMetaFileBits, SetWinMetaFileBits function [Windows GDI], _win32_SetWinMetaFileBits, gdi.setwinmetafilebits, wingdi/SetWinMetaFileBits
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
 - SetWinMetaFileBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetWinMetaFileBits function


## -description


The <b>SetWinMetaFileBits</b> function converts a metafile from the older Windows format to the new enhanced format and stores the new metafile in memory.


## -parameters




### -param nSize [in]

The size, in bytes, of the buffer that contains the Windows-format metafile.


### -param lpMeta16Data [in]

A pointer to a buffer that contains the Windows-format metafile data. (It is assumed that the data was obtained by using the <a href="https://msdn.microsoft.com/6ca6de2e-79cb-4503-a0d7-f616b8e383eb">GetMetaFileBitsEx</a> or <a href="https://msdn.microsoft.com/db61ea3a-44d0-4769-acb4-05a982d3f06f">GetWinMetaFileBits</a> function.)


### -param hdcRef [in]

A handle to a reference device context.


### -param lpMFP [in]

A pointer to a <a href="_win32_METAFILEPICT_str_cpp">METAFILEPICT</a> structure that contains the suggested size of the metafile picture and the mapping mode that was used when the picture was created.


## -returns



If the function succeeds, the return value is a handle to a memory-based enhanced metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Windows uses the reference device context's resolution data and the data in the <a href="_win32_METAFILEPICT_str_cpp">METAFILEPICT</a> structure to scale a picture. If the <i>hdcRef</i> parameter is <b>NULL</b>, the system uses resolution data for the current output device. If the <i>lpmfp</i> parameter is <b>NULL</b>, the system uses the MM_ANISOTROPIC mapping mode to scale the picture so that it fits the entire device surface. The <b>hMF</b> member of the <b>METAFILEPICT</b> structure is not used.

When the application no longer needs the enhanced metafile handle, it should delete it by calling the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function.

The handle returned by this function can be used with other enhanced-metafile functions.

If the reference device context is not identical to the device in which the metafile was originally created, some GDI functions that use device units may not draw the picture correctly.




## -see-also




<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/6ca6de2e-79cb-4503-a0d7-f616b8e383eb">GetMetaFileBitsEx</a>



<a href="https://msdn.microsoft.com/db61ea3a-44d0-4769-acb4-05a982d3f06f">GetWinMetaFileBits</a>



<a href="_win32_METAFILEPICT_str_cpp">METAFILEPICT</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>
 

 


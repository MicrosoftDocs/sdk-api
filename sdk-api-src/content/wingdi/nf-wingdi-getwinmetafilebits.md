---
UID: NF:wingdi.GetWinMetaFileBits
title: GetWinMetaFileBits function
author: windows-sdk-content
description: The GetWinMetaFileBits function converts the enhanced-format records from a metafile into Windows-format records and stores the converted records in the specified buffer.
old-location: gdi\getwinmetafilebits.htm
tech.root: gdi
ms.assetid: db61ea3a-44d0-4769-acb4-05a982d3f06f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetWinMetaFileBits, GetWinMetaFileBits function [Windows GDI], _win32_GetWinMetaFileBits, gdi.getwinmetafilebits, wingdi/GetWinMetaFileBits
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
 - Ext-MS-Win-GDI-Metafile-l1-1-1.dll
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - GDI32Full.dll
api_name:
 - GetWinMetaFileBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWinMetaFileBits function


## -description


The <b>GetWinMetaFileBits</b> function converts the enhanced-format records from a metafile into Windows-format records and stores the converted records in the specified buffer.


## -parameters




### -param hemf [in]

A handle to the enhanced metafile.


### -param cbData16 [in]

The size, in bytes, of the buffer into which the converted records are to be copied.


### -param pData16 [out]

A pointer to the buffer that receives the converted records. If <i>lpbBuffer</i> is <b>NULL</b>, <b>GetWinMetaFileBits</b> returns the number of bytes required to store the converted metafile records.


### -param iMapMode [in]

The mapping mode to use in the converted metafile.


### -param hdcRef [in]

A handle to the reference device context.


## -returns



If the function succeeds and the buffer pointer is <b>NULL</b>, the return value is the number of bytes required to store the converted records; if the function succeeds and the buffer pointer is a valid pointer, the return value is the size of the metafile data in bytes.

If the function fails, the return value is zero.




## -remarks



This function converts an enhanced metafile into a Windows-format metafile so that its picture can be displayed in an application that recognizes the older format.

The system uses the reference device context to determine the resolution of the converted metafile.

The <b>GetWinMetaFileBits</b> function does not invalidate the enhanced metafile handle. An application should call the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function to release the handle when it is no longer needed.

To create a scalable Windows-format metafile, specify MM_ANISOTROPIC as the <i>fnMapMode</i> parameter.

The upper-left corner of the metafile picture is always mapped to the origin of the reference device.




## -see-also




<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/a4d6a63a-6d2d-4bd9-9e71-4cd1b5f145a4">SetMapMode</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 


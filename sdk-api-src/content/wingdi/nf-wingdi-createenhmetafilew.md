---
UID: NF:wingdi.CreateEnhMetaFileW
title: CreateEnhMetaFileW function
author: windows-sdk-content
description: The CreateEnhMetaFile function creates a device context for an enhanced-format metafile. This device context can be used to store a device-independent picture.
old-location: gdi\createenhmetafile.htm
tech.root: gdi
ms.assetid: 647f83ca-dca3-44af-a594-5f9ba2bd7607
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CreateEnhMetaFile, CreateEnhMetaFile function [Windows GDI], CreateEnhMetaFileA, CreateEnhMetaFileW, _win32_CreateEnhMetaFile, gdi.createenhmetafile, wingdi/CreateEnhMetaFile, wingdi/CreateEnhMetaFileA, wingdi/CreateEnhMetaFileW
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
req.unicode-ansi: CreateEnhMetaFileW (Unicode) and CreateEnhMetaFileA (ANSI)
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
 - ext-ms-win-gdi-metafile-l1-1-2.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateEnhMetaFile
 - CreateEnhMetaFileA
 - CreateEnhMetaFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateEnhMetaFileW function


## -description


The <b>CreateEnhMetaFile</b> function creates a device context for an enhanced-format metafile. This device context can be used to store a device-independent picture.


## -parameters




### -param hdc [in]

A handle to a reference device for the enhanced metafile. This parameter can be <b>NULL</b>; for more information, see Remarks.


### -param lpFilename [in]

A pointer to the file name for the enhanced metafile to be created. If this parameter is <b>NULL</b>, the enhanced metafile is memory based and its contents are lost when it is deleted by using the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function.


### -param lprc [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the dimensions (in .01-millimeter units) of the picture to be stored in the enhanced metafile.


### -param lpDesc [in]

A pointer to a string that specifies the name of the application that created the picture, as well as the picture's title. This parameter can be <b>NULL</b>; for more information, see Remarks.


## -returns



If the function succeeds, the return value is a handle to the device context for the enhanced metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Where text arguments must use Unicode characters, use the <b>CreateEnhMetaFile</b> function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

The system uses the reference device identified by the <i>hdcRef</i> parameter to record the resolution and units of the device on which a picture originally appeared. If the <i>hdcRef</i> parameter is <b>NULL</b>, it uses the current display device for reference.

The <b>left</b> and <b>top</b> members of the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure pointed to by the <i>lpRect</i> parameter must be less than the <b>right</b> and <b>bottom</b> members, respectively. Points along the edges of the rectangle are included in the picture. If <i>lpRect</i> is <b>NULL</b>, the graphics device interface (GDI) computes the dimensions of the smallest rectangle that surrounds the picture drawn by the application. The <i>lpRect</i> parameter should be provided where possible.

The string pointed to by the <i>lpDescription</i> parameter must contain a null character between the application name and the picture name and must terminate with two null charactersfor example, "XYZ Graphics Editor\0Bald Eagle\0\0", where \0 represents the null character. If <i>lpDescription</i> is <b>NULL</b>, there is no corresponding entry in the enhanced-metafile header.

Applications use the device context created by this function to store a graphics picture in an enhanced metafile. The handle identifying this device context can be passed to any GDI function.

After an application stores a picture in an enhanced metafile, it can display the picture on any output device by calling the <a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a> function. When displaying the picture, the system uses the rectangle pointed to by the <i>lpRect</i> parameter and the resolution data from the reference device to position and scale the picture.

The device context returned by this function contains the same default attributes associated with any new device context.

Applications must use the <a href="https://msdn.microsoft.com/db61ea3a-44d0-4769-acb4-05a982d3f06f">GetWinMetaFileBits</a> function to convert an enhanced metafile to the older Windows metafile format.

The file name for the enhanced metafile should use the .emf extension.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/084b2737-eb55-4587-b8e8-3eb3fa3688c4">Creating an Enhanced Metafile</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3c4a0d8b-75a5-4729-8c64-476c36d01a90">CloseEnhMetaFile</a>



<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/51f4f617-fe53-4463-b222-cb6860d15dd6">GetEnhMetaFileDescription</a>



<a href="https://msdn.microsoft.com/c42bcbe2-2e8f-42bd-a8e3-2827c6563300">GetEnhMetaFileHeader</a>



<a href="https://msdn.microsoft.com/db61ea3a-44d0-4769-acb4-05a982d3f06f">GetWinMetaFileBits</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>
 

 


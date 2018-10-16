---
UID: NF:wingdi.CreateMetaFileW
title: CreateMetaFileW function
author: windows-sdk-content
description: The CreateMetaFile function creates a device context for a Windows-format metafile.
old-location: gdi\createmetafile.htm
tech.root: gdi
ms.assetid: 81b3baae-f0e6-4b71-a6de-953ad3376dbd
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CreateMetaFile, CreateMetaFile function [Windows GDI], CreateMetaFileA, CreateMetaFileW, _win32_CreateMetaFile, gdi.createmetafile, wingdi/CreateMetaFile, wingdi/CreateMetaFileA, wingdi/CreateMetaFileW
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
req.unicode-ansi: CreateMetaFileW (Unicode) and CreateMetaFileA (ANSI)
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateMetaFile
 - CreateMetaFileA
 - CreateMetaFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateMetaFileW function


## -description


The <b>CreateMetaFile</b> function creates a device context for a Windows-format metafile.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/647f83ca-dca3-44af-a594-5f9ba2bd7607">CreateEnhMetaFile</a>.</div><div> </div>

## -parameters




### -param pszFile [in]

A pointer to the file name for the Windows-format metafile to be created. If this parameter is <b>NULL</b>, the Windows-format metafile is memory based and its contents are lost when it is deleted by using the <a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a> function.


## -returns



If the function succeeds, the return value is a handle to the device context for the Windows-format metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Where text arguments must use Unicode characters, use the <b>CreateMetaFile</b> function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

<b>CreateMetaFile</b> is a Windows-format metafile function. This function supports only 16-bit Windows-based applications, which are listed in <a href="https://msdn.microsoft.com/ebbf871b-cf78-4a90-8f27-e44699c17178">Windows-Format Metafiles</a>. It does not record or play back GDI functions such as <a href="https://msdn.microsoft.com/d1622574-c65e-4265-9a17-22bb4d2cae0e">PolyBezier</a>, which were not part of 16-bit Windows.

The device context created by this function can be used to record GDI output functions in a Windows-format metafile. It cannot be used with GDI query functions such as <a href="https://msdn.microsoft.com/d3d91b86-5143-431a-ba18-b951b832d7b6">GetTextColor</a>. When the device context is used with a GDI output function, the return value of that function becomes <b>TRUE</b> if the function is recorded and <b>FALSE</b> otherwise. When an object is selected by using the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function, only a copy of the object is recorded. The object still belongs to the application.

To create a scalable Windows-format metafile, record the graphics output in the MM_ANISOTROPIC mapping mode. The file cannot contain functions that modify the viewport origin and extents, nor can it contain device-dependent functions such as the <a href="https://msdn.microsoft.com/7a4f0b9c-8588-4da8-a030-ed9d8b4ee08d">SelectClipRgn</a> function. Once created, the Windows metafile can be scaled and rendered to any output device-format by defining the viewport origin and extents of the picture before playing it.




## -see-also




<a href="https://msdn.microsoft.com/8e50457a-8ef8-4e71-8c56-38cfb277f57d">CloseMetaFile</a>



<a href="https://msdn.microsoft.com/647f83ca-dca3-44af-a594-5f9ba2bd7607">CreateEnhMetaFile</a>



<a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a>



<a href="https://msdn.microsoft.com/d3d91b86-5143-431a-ba18-b951b832d7b6">GetTextColor</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/7a4f0b9c-8588-4da8-a030-ed9d8b4ee08d">SelectClipRgn</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 


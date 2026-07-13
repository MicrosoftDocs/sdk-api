---
UID: NF:wingdi.CreateEnhMetaFileA
title: CreateEnhMetaFileA function (wingdi.h)
description: The CreateEnhMetaFile function creates a device context for an enhanced-format metafile. This device context can be used to store a device-independent picture. (ANSI)
helpviewer_keywords: ["CreateEnhMetaFileA", "wingdi/CreateEnhMetaFileA"]
old-location: gdi\createenhmetafile.htm
tech.root: gdi
ms.assetid: 647f83ca-dca3-44af-a594-5f9ba2bd7607
ms.date: 12/05/2018
ms.keywords: CreateEnhMetaFile, CreateEnhMetaFile function [Windows GDI], CreateEnhMetaFileA, CreateEnhMetaFileW, _win32_CreateEnhMetaFile, gdi.createenhmetafile, wingdi/CreateEnhMetaFile, wingdi/CreateEnhMetaFileA, wingdi/CreateEnhMetaFileW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateEnhMetaFileA
 - wingdi/CreateEnhMetaFileA
dev_langs:
 - c++
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
---

# CreateEnhMetaFileA function


## -description

The <b>CreateEnhMetaFile</b> function creates a device context for an enhanced-format metafile. This device context can be used to store a device-independent picture.

## -parameters

### -param hdc [in]

A handle to a reference device for the enhanced metafile. This parameter can be <b>NULL</b>; for more information, see Remarks.

### -param lpFilename [in]

A pointer to the file name for the enhanced metafile to be created. If this parameter is <b>NULL</b>, the enhanced metafile is memory based and its contents are lost when it is deleted by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a> function.

### -param lprc [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the dimensions (in .01-millimeter units) of the picture to be stored in the enhanced metafile.

### -param lpDesc [in]

A pointer to a string that specifies the name of the application that created the picture, as well as the picture's title. This parameter can be <b>NULL</b>; for more information, see Remarks.

## -returns

If the function succeeds, the return value is a handle to the device context for the enhanced metafile.

If the function fails, the return value is <b>NULL</b>.

## -remarks

Where text arguments must use Unicode characters, use the <b>CreateEnhMetaFile</b> function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

The system uses the reference device identified by the <i>hdcRef</i> parameter to record the resolution and units of the device on which a picture originally appeared. If the <i>hdcRef</i> parameter is <b>NULL</b>, it uses the current display device for reference.

The <b>left</b> and <b>top</b> members of the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure pointed to by the <i>lpRect</i> parameter must be less than the <b>right</b> and <b>bottom</b> members, respectively. Points along the edges of the rectangle are included in the picture. If <i>lpRect</i> is <b>NULL</b>, the graphics device interface (GDI) computes the dimensions of the smallest rectangle that surrounds the picture drawn by the application. The <i>lpRect</i> parameter should be provided where possible.

The string pointed to by the <i>lpDescription</i> parameter must contain a null character between the application name and the picture name and must terminate with two null characters, for example, "XYZ Graphics Editor\0Bald Eagle\0\0", where \0 represents the null character. If <i>lpDescription</i> is <b>NULL</b>, there is no corresponding entry in the enhanced-metafile header.

Applications use the device context created by this function to store a graphics picture in an enhanced metafile. The handle identifying this device context can be passed to any GDI function.

After an application stores a picture in an enhanced metafile, it can display the picture on any output device by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a> function. When displaying the picture, the system uses the rectangle pointed to by the <i>lpRect</i> parameter and the resolution data from the reference device to position and scale the picture.

The device context returned by this function contains the same default attributes associated with any new device context.

Applications must use the <a href="/windows/desktop/api/wingdi/nf-wingdi-getwinmetafilebits">GetWinMetaFileBits</a> function to convert an enhanced metafile to the older Windows metafile format.

The file name for the enhanced metafile should use the .emf extension.


#### Examples

For an example, see <a href="/windows/desktop/gdi/creating-an-enhanced-metafile">Creating an Enhanced Metafile</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines CreateEnhMetaFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-closeenhmetafile">CloseEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteenhmetafile">DeleteEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafiledescriptiona">GetEnhMetaFileDescription</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getenhmetafileheader">GetEnhMetaFileHeader</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getwinmetafilebits">GetWinMetaFileBits</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>

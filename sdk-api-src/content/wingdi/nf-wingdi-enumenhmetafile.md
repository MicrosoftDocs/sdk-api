---
UID: NF:wingdi.EnumEnhMetaFile
title: EnumEnhMetaFile function (wingdi.h)
description: The EnumEnhMetaFile function enumerates the records within an enhanced-format metafile by retrieving each record and passing it to the specified callback function.
helpviewer_keywords: ["EnumEnhMetaFile","EnumEnhMetaFile function [Windows GDI]","_win32_EnumEnhMetaFile","gdi.enumenhmetafile","wingdi/EnumEnhMetaFile"]
old-location: gdi\enumenhmetafile.htm
tech.root: gdi
ms.assetid: bef5f43e-219a-4f8a-986d-290e29e17c4e
ms.date: 12/05/2018
ms.keywords: EnumEnhMetaFile, EnumEnhMetaFile function [Windows GDI], _win32_EnumEnhMetaFile, gdi.enumenhmetafile, wingdi/EnumEnhMetaFile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnumEnhMetaFile
 - wingdi/EnumEnhMetaFile
dev_langs:
 - c++
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
 - EnumEnhMetaFile
---

# EnumEnhMetaFile function


## -description

The <b>EnumEnhMetaFile</b> function enumerates the records within an enhanced-format metafile by retrieving each record and passing it to the specified callback function. The application-supplied callback function processes each record as required. The enumeration continues until the last record is processed or when the callback function returns zero.

## -parameters

### -param hdc [in]

A handle to a device context. This handle is passed to the callback function.

### -param hmf [in]

A handle to an enhanced metafile.

### -param proc [in]

A pointer to the application-supplied callback function. For more information, see the <a href="/previous-versions/dd162606(v=vs.85)">EnhMetaFileProc</a> function.

### -param param [in]

A pointer to optional callback-function data.

### -param lpRect [in]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the coordinates, in logical units, of the picture's upper-left and lower-right corners.

## -returns

If the callback function successfully enumerates all the records in the enhanced metafile, the return value is nonzero.

If the callback function does not successfully enumerate all the records in the enhanced metafile, the return value is zero.

## -remarks

Points along the edge of the rectangle pointed to by the <i>lpRect</i> parameter are included in the picture. If the <i>hdc</i> parameter is <b>NULL</b>, the system ignores <i>lpRect</i>.

If the callback function calls the <a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafilerecord">PlayEnhMetaFileRecord</a> function, <i>hdc</i> must identify a valid device context. The system uses the device context's transformation and mapping mode to transform the picture displayed by the <b>PlayEnhMetaFileRecord</b> function.

You can use the <b>EnumEnhMetaFile</b> function to embed one enhanced-metafile within another.

## -see-also

<a href="/previous-versions/dd162606(v=vs.85)">EnhMetaFileProc</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafile">PlayEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-playenhmetafilerecord">PlayEnhMetaFileRecord</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>
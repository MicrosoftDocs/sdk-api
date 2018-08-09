---
UID: NF:wingdi.EnumEnhMetaFile
title: EnumEnhMetaFile function
author: windows-sdk-content
description: The EnumEnhMetaFile function enumerates the records within an enhanced-format metafile by retrieving each record and passing it to the specified callback function.
old-location: gdi\enumenhmetafile.htm
old-project: gdi
ms.assetid: bef5f43e-219a-4f8a-986d-290e29e17c4e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumEnhMetaFile, EnumEnhMetaFile function [Windows GDI], _win32_EnumEnhMetaFile, gdi.enumenhmetafile, wingdi/EnumEnhMetaFile
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
 - EnumEnhMetaFile
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
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

A pointer to the application-supplied callback function. For more information, see the <a href="https://msdn.microsoft.com/c9f04b38-18bc-4b52-8c56-d9475bc30202">EnhMetaFileProc</a> function.


### -param param [in]

A pointer to optional callback-function data.


### -param lpRect [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the coordinates, in logical units, of the picture's upper-left and lower-right corners.


## -returns



If the callback function successfully enumerates all the records in the enhanced metafile, the return value is nonzero.

If the callback function does not successfully enumerate all the records in the enhanced metafile, the return value is zero.




## -remarks



Points along the edge of the rectangle pointed to by the <i>lpRect</i> parameter are included in the picture. If the <i>hdc</i> parameter is <b>NULL</b>, the system ignores <i>lpRect</i>.

If the callback function calls the <a href="https://msdn.microsoft.com/3eec8c8d-b99f-4500-9d18-b819c097f341">PlayEnhMetaFileRecord</a> function, <i>hdc</i> must identify a valid device context. The system uses the device context's transformation and mapping mode to transform the picture displayed by the <b>PlayEnhMetaFileRecord</b> function.

You can use the <b>EnumEnhMetaFile</b> function to embed one enhanced-metafile within another.




## -see-also




<a href="https://msdn.microsoft.com/c9f04b38-18bc-4b52-8c56-d9475bc30202">EnhMetaFileProc</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>



<a href="https://msdn.microsoft.com/3eec8c8d-b99f-4500-9d18-b819c097f341">PlayEnhMetaFileRecord</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>
 

 


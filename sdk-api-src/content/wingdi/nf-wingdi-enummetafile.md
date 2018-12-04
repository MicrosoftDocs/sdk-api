---
UID: NF:wingdi.EnumMetaFile
title: EnumMetaFile function
author: windows-sdk-content
description: The EnumMetaFile function enumerates the records within a Windows-format metafile by retrieving each record and passing it to the specified callback function.
old-location: gdi\enummetafile.htm
tech.root: gdi
ms.assetid: b11c7467-64a9-442b-8dee-26e15f64a26b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EnumMetaFile, EnumMetaFile function [Windows GDI], _win32_EnumMetaFile, gdi.enummetafile, wingdi/EnumMetaFile
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
 - EnumMetaFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnumMetaFile function


## -description


The <b>EnumMetaFile</b> function enumerates the records within a Windows-format metafile by retrieving each record and passing it to the specified callback function. The application-supplied callback function processes each record as required. The enumeration continues until the last record is processed or when the callback function returns zero.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>.</div><div> </div>

## -parameters




### -param hdc [in]

Handle to a device context. This handle is passed to the callback function.


### -param hmf [in]

Handle to a Windows-format metafile.


### -param proc [in]

Pointer to an application-supplied callback function. For more information, see <a href="https://msdn.microsoft.com/ebef5a3f-0dd7-49df-a07d-c55c5e8c868c">EnumMetaFileProc</a>.


### -param param [in]

Pointer to optional data.


## -returns



If the callback function successfully enumerates all the records in the Windows-format metafile, the return value is nonzero.

If the callback function does not successfully enumerate all the records in the Windows-format metafile, the return value is zero.




## -remarks



To convert a Windows-format metafile into an enhanced-format metafile, use the <a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a> function.

You can use the <b>EnumMetaFile</b> function to embed one Windows-format metafile within another.




## -see-also




<a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>



<a href="https://msdn.microsoft.com/ebef5a3f-0dd7-49df-a07d-c55c5e8c868c">EnumMetaFileProc</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/044894df-dc8a-41b2-8810-e0a1b8bc19d8">PlayMetaFile</a>



<a href="https://msdn.microsoft.com/bea22981-dc77-4de2-b6dc-d6a4f4b74bbd">PlayMetaFileRecord</a>



<a href="https://msdn.microsoft.com/b7170c8a-da5f-4946-9c56-da3cffc84567">SetWinMetaFileBits</a>
 

 


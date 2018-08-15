---
UID: NF:wingdi.PlayEnhMetaFileRecord
title: PlayEnhMetaFileRecord function
author: windows-sdk-content
description: The PlayEnhMetaFileRecord function plays an enhanced-metafile record by executing the graphics device interface (GDI) functions identified by the record.
old-location: gdi\playenhmetafilerecord.htm
old-project: gdi
ms.assetid: 3eec8c8d-b99f-4500-9d18-b819c097f341
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PlayEnhMetaFileRecord, PlayEnhMetaFileRecord function [Windows GDI], _win32_PlayEnhMetaFileRecord, gdi.playenhmetafilerecord, wingdi/PlayEnhMetaFileRecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.redist: 
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
 - PlayEnhMetaFileRecord
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PlayEnhMetaFileRecord function


## -description


The <b>PlayEnhMetaFileRecord</b> function plays an enhanced-metafile record by executing the graphics device interface (GDI) functions identified by the record.


## -parameters




### -param hdc [in]

A handle to the device context passed to the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function.


### -param pht [in]

A pointer to a table of handles to GDI objects used when playing the metafile. The first entry in this table contains the enhanced-metafile handle.


### -param pmr [in]

A pointer to the enhanced-metafile record to be played.


### -param cht [in]

The number of handles in the handle table.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



This is an enhanced-metafile function.

An application typically uses <b>PlayEnhMetaFileRecord</b> in conjunction with the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function to process and play an enhanced-format metafile one record at a time.

The <i>hdc</i>, <i>lpHandletable</i>, and <i>nHandles</i> parameters must be exactly those passed to the <a href="https://msdn.microsoft.com/c9f04b38-18bc-4b52-8c56-d9475bc30202">EnhMetaFileProc</a> callback procedure by the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function.

If <b>PlayEnhMetaFileRecord</b> does not recognize a record, it ignores the record and returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>



<a href="https://msdn.microsoft.com/51e8937b-0c42-49fe-8930-7af303fce788">PlayEnhMetaFile</a>
 

 


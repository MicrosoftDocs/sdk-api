---
UID: NC:wingdi.ENHMFENUMPROC
title: ENHMFENUMPROC (wingdi.h)
author: windows-sdk-content
description: The EnhMetaFileProc function is an application-defined callback function used with the EnumEnhMetaFile function.
old-location: gdi\enhmetafileproc.htm
tech.root: gdi
ms.assetid: c9f04b38-18bc-4b52-8c56-d9475bc30202
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ENHMFENUMPROC, ENHMFENUMPROC callback, ENHMFENUMPROC callback function [Windows GDI], _win32_EnhMetaFileProc, gdi.enhmetafileproc, wingdi/ENHMFENUMPROC
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - ENHMFENUMPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ENHMFENUMPROC callback function


## -description


The <b>EnhMetaFileProc</b> function is an application-defined callback function used with the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function. The <b>ENHMFENUMPROC</b> type defines a pointer to this callback function. <b>EnhMetaFileProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param hdc


### -param *lpht


### -param *lpmr


### -param nHandles


### -param data








#### - hDC [in]

Handle to the device context passed to <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>.


#### - lpData [in]

Pointer to optional data.


#### - lpEMFR [in]

Pointer to one of the records in the metafile. This record should not be modified. (If modification is necessary, it should be performed on a copy of the record.)


#### - lpHTable [in]

Pointer to a <a href="https://msdn.microsoft.com/c0c03c7d-baac-4b59-ba2f-8f6330651b49">HANDLETABLE</a> structure representing the table of handles associated with the graphics objects (pens, brushes, and so on) in the metafile. The first entry contains the enhanced-metafile handle.


#### - nObj [in]

Specifies the number of objects with associated handles in the handle table.


## -returns



This function must return a nonzero value to continue enumeration; to stop enumeration, it must return zero.




## -remarks



An application must register the callback function by passing its address to the <a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/efe49094-fe61-40e1-873e-3302c595717e">ENHMETARECORD</a>



<a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>



<a href="https://msdn.microsoft.com/c0c03c7d-baac-4b59-ba2f-8f6330651b49">HANDLETABLE</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


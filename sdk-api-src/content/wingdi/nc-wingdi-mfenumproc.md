---
UID: NC:wingdi.MFENUMPROC
title: MFENUMPROC
author: windows-sdk-content
description: The EnumMetaFileProc function is an application-defined callback function that processes Windows-format metafile records.
old-location: gdi\enummetafileproc.htm
tech.root: gdi
ms.assetid: ebef5a3f-0dd7-49df-a07d-c55c5e8c868c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MFENUMPROC, MFENUMPROC callback, MFENUMPROC callback function [Windows GDI], _win32_EnumMetaFileProc, gdi.enummetafileproc, wingdi/MFENUMPROC
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MFENUMPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFENUMPROC callback function


## -description


The <b>EnumMetaFileProc</b> function is an application-defined callback function that processes Windows-format metafile records. This function is called by the <a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a> function. The <b>MFENUMPROC</b> type defines a pointer to this callback function. <b>EnumMetaFileProc</b> is a placeholder for the application-defined function name.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with Windows-format metafiles. Enhanced-format metafiles provide superior functionality and are recommended for new applications. The corresponding function for an enhanced-format metafile is <a href="https://msdn.microsoft.com/c9f04b38-18bc-4b52-8c56-d9475bc30202">EnhMetaFileProc</a>.</div><div> </div>

## -parameters




### -param hdc


### -param *lpht


### -param *lpMR


### -param nObj [in]

Specifies the number of objects with associated handles in the handle table.


### -param param








#### - hDC [in]

Handle to the device context passed to <a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a>.


#### - lpClientData [in]

Pointer to optional data.


#### - lpHTable [in]

Pointer to a table of handles associated with the graphics objects (pens, brushes, and so on) in the metafile.


#### - lpMFR [in]

Pointer to one of the records in the metafile. This record should not be modified. (If modification is necessary, it should be performed on a copy of the record.)


## -returns



This function must return a nonzero value to continue enumeration; to stop enumeration, it must return zero.




## -remarks



An application must register the callback function by passing its address to the <a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a> function.

<b>EnumMetaFileProc</b> is a placeholder for the application-supplied function name.




## -see-also




<a href="https://msdn.microsoft.com/c9f04b38-18bc-4b52-8c56-d9475bc30202">EnhMetaFileProc</a>



<a href="https://msdn.microsoft.com/bef5f43e-219a-4f8a-986d-290e29e17c4e">EnumEnhMetaFile</a>



<a href="https://msdn.microsoft.com/b11c7467-64a9-442b-8dee-26e15f64a26b">EnumMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 


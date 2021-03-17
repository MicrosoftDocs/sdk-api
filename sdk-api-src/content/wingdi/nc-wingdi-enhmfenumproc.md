---
UID: NC:wingdi.ENHMFENUMPROC
title: ENHMFENUMPROC (wingdi.h)
description: The EnhMetaFileProc function is an application-defined callback function used with the EnumEnhMetaFile function.
helpviewer_keywords: ["ENHMFENUMPROC","ENHMFENUMPROC callback","ENHMFENUMPROC callback function [Windows GDI]","_win32_EnhMetaFileProc","gdi.enhmetafileproc","wingdi/ENHMFENUMPROC"]
old-location: gdi\enhmetafileproc.htm
tech.root: gdi
ms.assetid: c9f04b38-18bc-4b52-8c56-d9475bc30202
ms.date: 12/05/2018
ms.keywords: ENHMFENUMPROC, ENHMFENUMPROC callback, ENHMFENUMPROC callback function [Windows GDI], _win32_EnhMetaFileProc, gdi.enhmetafileproc, wingdi/ENHMFENUMPROC
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ENHMFENUMPROC
 - wingdi/ENHMFENUMPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - ENHMFENUMPROC
---

# ENHMFENUMPROC callback function


## -description

The <b>EnhMetaFileProc</b> function is an application-defined callback function used with the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a> function. The <b>ENHMFENUMPROC</b> type defines a pointer to this callback function. <b>EnhMetaFileProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param hdc

### -param lpht

### -param lpmr

### -param nHandles

### -param data

### -param hDC [in]

Handle to the device context passed to <a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a>.


#### - lpData [in]

Pointer to optional data.


#### - lpEMFR [in]

Pointer to one of the records in the metafile. This record should not be modified. (If modification is necessary, it should be performed on a copy of the record.)


#### - lpHTable [in]

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-handletable">HANDLETABLE</a> structure representing the table of handles associated with the graphics objects (pens, brushes, and so on) in the metafile. The first entry contains the enhanced-metafile handle.


#### - nObj [in]

Specifies the number of objects with associated handles in the handle table.

## -returns

This function must return a nonzero value to continue enumeration; to stop enumeration, it must return zero.

## -remarks

An application must register the callback function by passing its address to the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a> function.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetarecord">ENHMETARECORD</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumenhmetafile">EnumEnhMetaFile</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-handletable">HANDLETABLE</a>



<a href="/windows/desktop/gdi/metafile-functions">Metafile Functions</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>

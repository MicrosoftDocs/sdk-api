---
UID: NC:wingdi.GOBJENUMPROC
title: GOBJENUMPROC (wingdi.h)
description: The EnumObjectsProc function is an application-defined callback function used with the EnumObjects function.
helpviewer_keywords: ["GOBJENUMPROC","GOBJENUMPROC callback","GOBJENUMPROC callback function [Windows GDI]","_win32_EnumObjectsProc","gdi.enumobjectsproc","wingdi/GOBJENUMPROC"]
old-location: gdi\enumobjectsproc.htm
tech.root: gdi
ms.assetid: 05a0f329-add9-4e92-9a9a-e2cf0ba5a1c3
ms.date: 12/05/2018
ms.keywords: GOBJENUMPROC, GOBJENUMPROC callback, GOBJENUMPROC callback function [Windows GDI], _win32_EnumObjectsProc, gdi.enumobjectsproc, wingdi/GOBJENUMPROC
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
 - GOBJENUMPROC
 - wingdi/GOBJENUMPROC
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
 - GOBJENUMPROC
---

# GOBJENUMPROC callback function


## -description

The <b>EnumObjectsProc</b> function is an application-defined callback function used with the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumobjects">EnumObjects</a> function. It is used to process the object data. The <b>GOBJENUMPROC</b> type defines a pointer to this callback function. <b>EnumObjectsProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

### -param unnamedParam2

#### - lpData [in]

A pointer to the application-defined data passed by the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumobjects">EnumObjects</a> function.


#### - lpLogObject [in]

A pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logpen">LOGPEN</a> or <a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a> structure describing the attributes of the object.

## -returns

To continue enumeration, the callback function must return a nonzero value. This value is user-defined.

To stop enumeration, the callback function must return zero.

## -remarks

An application must register this function by passing its address to the <a href="/windows/desktop/api/wingdi/nf-wingdi-enumobjects">EnumObjects</a> function.

## -see-also

<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-enumobjects">EnumObjects</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a>



<a href="/windows/desktop/api/winbase/nf-winbase-globallock">GlobalLock</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logpen">LOGPEN</a>
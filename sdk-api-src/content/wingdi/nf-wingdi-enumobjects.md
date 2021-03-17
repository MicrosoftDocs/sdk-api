---
UID: NF:wingdi.EnumObjects
title: EnumObjects function (wingdi.h)
description: The EnumObjects function enumerates the pens or brushes available for the specified device context (DC).
helpviewer_keywords: ["EnumObjects","EnumObjects function [Windows GDI]","_win32_EnumObjects","gdi.enumobjects","wingdi/EnumObjects"]
old-location: gdi\enumobjects.htm
tech.root: gdi
ms.assetid: 2a7b60b2-9a68-4c56-9376-c1b780488535
ms.date: 12/05/2018
ms.keywords: EnumObjects, EnumObjects function [Windows GDI], _win32_EnumObjects, gdi.enumobjects, wingdi/EnumObjects
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
 - EnumObjects
 - wingdi/EnumObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-L1-2-1.dll
 - GDI32Full.dll
api_name:
 - EnumObjects
---

# EnumObjects function


## -description

The <b>EnumObjects</b> function enumerates the pens or brushes available for the specified device context (DC). This function calls the application-defined callback function once for each available object, supplying data describing that object. <b>EnumObjects</b> continues calling the callback function until the callback function returns zero or until all of the objects have been enumerated.

## -parameters

### -param hdc [in]

A handle to the DC.

### -param nType [in]

The object type. This parameter can be OBJ_BRUSH or OBJ_PEN.

### -param lpFunc [in]

A pointer to the application-defined callback function. For more information about the callback function, see the <a href="/previous-versions/dd162686(v=vs.85)">EnumObjectsProc</a> function.

### -param lParam [in]

A pointer to the application-defined data. The data is passed to the callback function along with the object information.

## -returns

If the function succeeds, the return value is the last value returned by the callback function. Its meaning is user-defined.

If the objects cannot be enumerated (for example, there are too many objects), the function returns zero without calling the callback function.

## -see-also

<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/previous-versions/dd162686(v=vs.85)">EnumObjectsProc</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>
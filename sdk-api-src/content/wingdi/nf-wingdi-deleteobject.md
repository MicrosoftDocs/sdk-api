---
UID: NF:wingdi.DeleteObject
title: DeleteObject function (wingdi.h)
description: The DeleteObject function deletes a logical pen, brush, font, bitmap, region, or palette, freeing all system resources associated with the object. After the object is deleted, the specified handle is no longer valid.
helpviewer_keywords: ["DeleteObject","DeleteObject function [Windows GDI]","DeleteObjectW","_win32_DeleteObject","gdi.deleteobject","wingdi/DeleteObject","wingdi/DeleteObjectW"]
old-location: gdi\deleteobject.htm
tech.root: gdi
ms.assetid: cc679af0-6839-4c83-9c42-39d7ededda40
ms.date: 12/05/2018
ms.keywords: DeleteObject, DeleteObject function [Windows GDI], DeleteObjectW, _win32_DeleteObject, gdi.deleteobject, wingdi/DeleteObject, wingdi/DeleteObjectW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteObjectW (Unicode)
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
 - DeleteObject
 - wingdi/DeleteObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-object-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
api_name:
 - DeleteObject
 - DeleteObjectW
---

# DeleteObject function


## -description

The <b>DeleteObject</b> function deletes a logical pen, brush, font, bitmap, region, or palette, freeing all system resources associated with the object. After the object is deleted, the specified handle is no longer valid.

## -parameters

### -param ho [in]

A handle to a logical pen, brush, font, bitmap, region, or palette.

## -returns

If the function succeeds, the return value is nonzero.

If the specified handle is not valid or is currently selected into a DC, the return value is zero.

## -remarks

Do not delete a drawing object (pen or brush) while it is still selected into a DC.

When a pattern brush is deleted, the bitmap associated with the brush is not deleted. The bitmap must be deleted independently.


#### Examples

For an example, see <a href="/windows/desktop/gdi/creating-colored-pens-and-brushes">Creating Colored Pens and Brushes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>
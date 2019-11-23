---
UID: NF:wingdi.CreateDiscardableBitmap
title: CreateDiscardableBitmap function (wingdi.h)

description: The CreateDiscardableBitmap function creates a discardable bitmap that is compatible with the specified device.
old-location: gdi\creatediscardablebitmap.htm
tech.root: gdi
ms.assetid: 79168baf-26ea-4d24-b75c-d0658a56892c

ms.date: 12/05/2018
ms.keywords: CreateDiscardableBitmap, CreateDiscardableBitmap function [Windows GDI], _win32_CreateDiscardableBitmap, gdi.creatediscardablebitmap, wingdi/CreateDiscardableBitmap
ms.topic: function
f1_keywords: 
 - "wingdi/CreateDiscardableBitmap"
dev_langs:
 - c++
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - CreateDiscardableBitmap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateDiscardableBitmap function


## -description


The <b>CreateDiscardableBitmap</b> function creates a discardable bitmap that is compatible with the specified device. The bitmap has the same bits-per-pixel format and the same color palette as the device. An application can select this bitmap as the current bitmap for a memory device that is compatible with the specified device.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a> function.</div><div> </div>

## -parameters




### -param hdc [in]

A handle to a device context.


### -param cx [in]

The width, in pixels, of the bitmap.


### -param cy [in]

The height, in pixels, of the bitmap.


## -returns



If the function succeeds, the return value is a handle to the compatible bitmap (DDB).

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the bitmap, call the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmap-functions">Bitmap Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>
 

 


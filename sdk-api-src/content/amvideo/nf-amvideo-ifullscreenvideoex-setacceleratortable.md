---
UID: NF:amvideo.IFullScreenVideoEx.SetAcceleratorTable
title: IFullScreenVideoEx::SetAcceleratorTable (amvideo.h)
description: The SetAcceleratorTable method specifies an accelerator table that will be used to translate keyboard messages. The Full Screen Renderer filter does not support this method.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetAcceleratorTable method","IFullScreenVideoEx.SetAcceleratorTable","IFullScreenVideoEx::SetAcceleratorTable","IFullScreenVideoExSetAcceleratorTable","SetAcceleratorTable","SetAcceleratorTable method [DirectShow]","SetAcceleratorTable method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetAcceleratorTable","dshow.ifullscreenvideoex_setacceleratortable"]
old-location: dshow\ifullscreenvideoex_setacceleratortable.htm
tech.root: dshow
ms.assetid: aff393e8-e0a5-418d-8706-3fde96dbcfd9
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetAcceleratorTable method, IFullScreenVideoEx.SetAcceleratorTable, IFullScreenVideoEx::SetAcceleratorTable, IFullScreenVideoExSetAcceleratorTable, SetAcceleratorTable, SetAcceleratorTable method [DirectShow], SetAcceleratorTable method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetAcceleratorTable, dshow.ifullscreenvideoex_setacceleratortable
req.header: amvideo.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFullScreenVideoEx::SetAcceleratorTable
 - amvideo/IFullScreenVideoEx::SetAcceleratorTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.SetAcceleratorTable
---

# IFullScreenVideoEx::SetAcceleratorTable


## -description

The <code>SetAcceleratorTable</code> method specifies an accelerator table that will be used to translate keyboard messages. The Full Screen Renderer filter does not support this method.

## -parameters

### -param hwnd [in]

Handle of the window that will receive the translated messages.

### -param hAccel [in]

Handle to the accelerator table.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>
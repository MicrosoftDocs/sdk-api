---
UID: NF:mfidl.IMFVideoProcessorControl.SetBorderColor
title: IMFVideoProcessorControl::SetBorderColor (mfidl.h)
description: Sets the border color.
helpviewer_keywords: ["IMFVideoProcessorControl interface [Media Foundation]","SetBorderColor method","IMFVideoProcessorControl.SetBorderColor","IMFVideoProcessorControl::SetBorderColor","SetBorderColor","SetBorderColor method [Media Foundation]","SetBorderColor method [Media Foundation]","IMFVideoProcessorControl interface","mf.imfvideoprocessorcontrol_setbordercolor","mfidl/IMFVideoProcessorControl::SetBorderColor"]
old-location: mf\imfvideoprocessorcontrol_setbordercolor.htm
tech.root: mf
ms.assetid: DA6165C9-24E9-473C-A4F7-4C94399AF346
ms.date: 12/05/2018
ms.keywords: IMFVideoProcessorControl interface [Media Foundation],SetBorderColor method, IMFVideoProcessorControl.SetBorderColor, IMFVideoProcessorControl::SetBorderColor, SetBorderColor, SetBorderColor method [Media Foundation], SetBorderColor method [Media Foundation],IMFVideoProcessorControl interface, mf.imfvideoprocessorcontrol_setbordercolor, mfidl/IMFVideoProcessorControl::SetBorderColor
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFVideoProcessorControl::SetBorderColor
 - mfidl/IMFVideoProcessorControl::SetBorderColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoProcessorControl.SetBorderColor
---

# IMFVideoProcessorControl::SetBorderColor


## -description

Sets the border color.

## -parameters

### -param pBorderColor [in]

A pointer to an <a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfargb">MFARGB</a> structure that specifies the border color as an ARGB (alpha, red, green, blue) value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol">IMFVideoProcessorControl</a>
---
UID: NF:strmif.IVMRMixerBitmap.UpdateAlphaBitmapParameters
title: IVMRMixerBitmap::UpdateAlphaBitmapParameters (strmif.h)
description: The UpdateAlphaBitmapParameters method changes the bitmap location, size and blending value.
helpviewer_keywords: ["IVMRMixerBitmap interface [DirectShow]","UpdateAlphaBitmapParameters method","IVMRMixerBitmap.UpdateAlphaBitmapParameters","IVMRMixerBitmap::UpdateAlphaBitmapParameters","IVMRMixerBitmapUpdateAlphaBitmapParameters","UpdateAlphaBitmapParameters","UpdateAlphaBitmapParameters method [DirectShow]","UpdateAlphaBitmapParameters method [DirectShow]","IVMRMixerBitmap interface","dshow.ivmrmixerbitmap_updatealphabitmapparameters","strmif/IVMRMixerBitmap::UpdateAlphaBitmapParameters"]
old-location: dshow\ivmrmixerbitmap_updatealphabitmapparameters.htm
tech.root: dshow
ms.assetid: 039cb675-c384-4909-b06d-b331cc281df6
ms.date: 12/05/2018
ms.keywords: IVMRMixerBitmap interface [DirectShow],UpdateAlphaBitmapParameters method, IVMRMixerBitmap.UpdateAlphaBitmapParameters, IVMRMixerBitmap::UpdateAlphaBitmapParameters, IVMRMixerBitmapUpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters method [DirectShow], UpdateAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap interface, dshow.ivmrmixerbitmap_updatealphabitmapparameters, strmif/IVMRMixerBitmap::UpdateAlphaBitmapParameters
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IVMRMixerBitmap::UpdateAlphaBitmapParameters
 - strmif/IVMRMixerBitmap::UpdateAlphaBitmapParameters
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
 - IVMRMixerBitmap.UpdateAlphaBitmapParameters
---

# IVMRMixerBitmap::UpdateAlphaBitmapParameters


## -description

The <b>UpdateAlphaBitmapParameters</b> method changes the bitmap location, size and blending value.

## -parameters

### -param pBmpParms [in]

A pointer to a [VMRALPHABITMAP](/windows/desktop/api/strmif/ns-strmif-vmralphabitmap) structure.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The filter graph must be running for the changes to take effect. This method does not change the bitmap image. If you specify a [VMRALPHABITMAP](/windows/desktop/api/strmif/ns-strmif-vmralphabitmap) structure with no destination or color key set, the bitmap disappears. This behavior is by design for backward compatibility and cannot be changed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a>
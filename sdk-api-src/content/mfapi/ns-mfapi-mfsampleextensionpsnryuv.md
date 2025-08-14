---
UID: NS:mfapi._MFSampleExtensionPsnrYuv
tech.root: mf
title: MFSampleExtensionPsnrYuv
ms.date: 06/12/2025
targetos: Windows
description: Stores Peak Signal-to-Noise Ratio (PSNR) values for the Y, U, and V planes of an encoded video frame. 
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mfapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11, build 26100
req.target-min-winversvr:  Windows Server 2025
req.target-type: 
req.typenames: MFSampleExtensionPsnrYuv
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - _MFSampleExtensionPsnrYuv
 - MFSampleExtensionPsnrYuv
f1_keywords:
 - _MFSampleExtensionPsnrYuv
 - mfapi/_MFSampleExtensionPsnrYuv
 - MFSampleExtensionPsnrYuv
 - mfapi/MFSampleExtensionPsnrYuv
dev_langs:
 - c++
helpviewer_keywords:
 - _MFSampleExtensionPsnrYuv
---

## -description

Stores Peak Signal-to-Noise Ratio (PSNR) values for the Y, U, and V planes of an encoded video frame. PSNR is calculated by comparing the reconstructed frame to the original input frame.

## -struct-fields

### -field psnrY

The PSNR for the Y plane.

### -field psnrU

The PSNR for the U plane.

### -field psnrV

The PSNR for the V plane.

## -remarks

Use [IMFAttributes::SetUnknown](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to attach an [IMFMediaBuffer](/windows/win32/api/mfobjects/nn-mfobjects-imfmediabuffer) containing the PSNR values to an output sample. Use [IMFAttributes::GetUnknown](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to retrieve the **IMFMediaBuffer** containing the PSNR values from an output sample. The **IMFMediaBuffer** contains memory that matches the size of the **MFSampleExtensionPsnrYuv** structure. 

PSNR should only be reported when the entire frame has completed encoding. If the encoder uses multiple slices, the PSNR buffer should be attached to the [IMFSample](/windows/win32/api/mfobjects/nn-mfobjects-imfsample) of the last slice. 

If the encoder only supports PSNR for the Y plane, the *psnrU* and *psnrV* fields shall be zero. 

[MFCreateDXGISurfaceBuffer](/windows/win32/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer) can be used to convert a GPU resource into an **IMFMediaBuffer**. 

## -see-also


---
UID: NF:mfapi.MFCreateMediaBufferFromMediaType
title: MFCreateMediaBufferFromMediaType function (mfapi.h)
description: Allocates a system-memory buffer that is optimal for a specified media type.
old-location: mf\mfcreatemediabufferfrommediatype.htm
tech.root: medfound
ms.assetid: 1EBDB616-6FA9-4E4E-9BC6-CA1E382A08D9
ms.date: 12/05/2018
ms.keywords: MFCreateMediaBufferFromMediaType, MFCreateMediaBufferFromMediaType function [Media Foundation], mf.mfcreatemediabufferfrommediatype, mfapi/MFCreateMediaBufferFromMediaType
f1_keywords:
- mfapi/MFCreateMediaBufferFromMediaType
dev_langs:
- c++
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mfplat.dll
api_name:
- MFCreateMediaBufferFromMediaType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateMediaBufferFromMediaType function


## -description


Allocates a system-memory buffer that is optimal for a specified media type.


## -parameters




### -param pMediaType [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type.


### -param llDuration [in]

The sample duration. This value is required for audio formats.


### -param dwMinLength [in]

The minimum size of the buffer, in bytes. The actual buffer size might be larger. Specify zero to allocate the default buffer size for the media type.


### -param dwMinAlignment [in]

The minimum memory alignment for the buffer. Specify zero to use the default memory alignment.


### -param ppBuffer [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For video formats, if the format is recognized, the function creates a 2-D buffer that implements the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2">IMF2DBuffer2</a> interface. Otherwise it creates a linear buffer. To get the  <b>IMF2DBuffer2</b> interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the pointer returned in <i>ppBuffer</i>. If the <b>QueryInterface</b> method fails, use the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface to access the buffer memory.

For audio formats, the function allocates a buffer that is large enough to contain <i>llDuration</i> audio samples, or <i>dwMinLength</i>, whichever is larger.

This function always allocates system memory. For Direct3D surfaces, use the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer">MFCreateDXGISurfaceBuffer</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer">MFCreateDXSurfaceBuffer</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 


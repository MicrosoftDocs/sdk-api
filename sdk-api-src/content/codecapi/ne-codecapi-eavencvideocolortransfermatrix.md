---
UID: NE:codecapi.eAVEncVideoColorTransferMatrix
title: eAVEncVideoColorTransferMatrix (codecapi.h)

description: Specifies the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space. This enumeration is used with the AVEncVideoInputColorTransferMatrix and AVEncVideoOutputColorTransferMatrix properties.
old-location: dshow\eavencvideocolortransfermatrix.htm
tech.root: DirectShow
ms.assetid: 6912cc24-9c67-4c52-9cb7-3decbb4ba8ac

ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncVideoColorTransferMatrix, codecapi/eAVEncVideoColorTransferMatrix_BT601, codecapi/eAVEncVideoColorTransferMatrix_BT709, codecapi/eAVEncVideoColorTransferMatrix_SMPTE240M, codecapi/eAVEncVideoColorTransferMatrix_SameAsSource, dshow.eavencvideocolortransfermatrix, eAVEncVideoColorTransferMatrix, eAVEncVideoColorTransferMatrix enumeration [DirectShow], eAVEncVideoColorTransferMatrixEnumeration, eAVEncVideoColorTransferMatrix_BT601, eAVEncVideoColorTransferMatrix_BT709, eAVEncVideoColorTransferMatrix_SMPTE240M, eAVEncVideoColorTransferMatrix_SameAsSource
ms.topic: enum
f1_keywords: 
 - "codecapi/eAVEncVideoColorTransferMatrix"
dev_langs:
 - c++
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorTransferMatrix
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# eAVEncVideoColorTransferMatrix enumeration


## -description



Specifies the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space. This enumeration is used with the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencvideoinputcolortransfermatrix-property">AVEncVideoInputColorTransferMatrix</a> and <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avencvideooutputcolortransfermatrix-property">AVEncVideoOutputColorTransferMatrix</a> properties.




## -enum-fields




### -field eAVEncVideoColorTransferMatrix_SameAsSource

Use the same transfer matrix as the input video. This flag applies to the <b>AVEncVideoOutputColorTransferMatrix</b> property only.


### -field eAVEncVideoColorTransferMatrix_BT709

ITU-R BT.709 transfer matrix.


### -field eAVEncVideoColorTransferMatrix_BT601

ITU-R BT.601 transfer matrix.


### -field eAVEncVideoColorTransferMatrix_SMPTE240M

SMPTE 240M transfer matrix.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
 

 


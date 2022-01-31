---
UID: NE:wincodec.WICJpegTransferMatrix
title: WICJpegTransferMatrix (wincodec.h)
description: Specifies conversion matrix from Y'Cb'Cr' to R'G'B'.
helpviewer_keywords: ["WICJpegTransferMatrix","WICJpegTransferMatrix enumeration [Windows Imaging Component]","WICJpegTransferMatrixBT601","WICJpegTransferMatrixIdentity","WICJpegTransferMatrix_FORCE_DWORD","wic.wicjpegtransfermatrix","wincodec/WICJpegTransferMatrix","wincodec/WICJpegTransferMatrixBT601","wincodec/WICJpegTransferMatrixIdentity","wincodec/WICJpegTransferMatrix_FORCE_DWORD"]
old-location: wic\wicjpegtransfermatrix.htm
tech.root: wic
ms.assetid: 393342C4-A906-4427-BEAA-842FF77C9E9D
ms.date: 12/05/2018
ms.keywords: WICJpegTransferMatrix, WICJpegTransferMatrix enumeration [Windows Imaging Component], WICJpegTransferMatrixBT601, WICJpegTransferMatrixIdentity, WICJpegTransferMatrix_FORCE_DWORD, wic.wicjpegtransfermatrix, wincodec/WICJpegTransferMatrix, wincodec/WICJpegTransferMatrixBT601, wincodec/WICJpegTransferMatrixIdentity, wincodec/WICJpegTransferMatrix_FORCE_DWORD
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: WICJpegTransferMatrix
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICJpegTransferMatrix
 - wincodec/WICJpegTransferMatrix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wincodec.h
api_name:
 - WICJpegTransferMatrix
---

# WICJpegTransferMatrix enumeration


## -description

Specifies conversion matrix from Y'Cb'Cr' to R'G'B'.

## -enum-fields

### -field WICJpegTransferMatrixIdentity:0

Specifies the identity transfer matrix.

### -field WICJpegTransferMatrixBT601:0x1

Specifies the BT601 transfer matrix.

### -field WICJpegTransferMatrix_FORCE_DWORD:0x7fffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used.

## -see-also

<a href="/windows/desktop/api/wincodec/ns-wincodec-wicjpegframeheader">WICJpegFrameHeader</a>

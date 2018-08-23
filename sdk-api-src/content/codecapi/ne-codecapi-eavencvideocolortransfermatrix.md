---
UID: NE:codecapi.eAVEncVideoColorTransferMatrix
title: eAVEncVideoColorTransferMatrix
author: windows-sdk-content
description: Specifies the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space. This enumeration is used with the AVEncVideoInputColorTransferMatrix and AVEncVideoOutputColorTransferMatrix properties.
old-location: dshow\eavencvideocolortransfermatrix.htm
old-project: DirectShow
ms.assetid: 6912cc24-9c67-4c52-9cb7-3decbb4ba8ac
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: codecapi/eAVEncVideoColorTransferMatrix, codecapi/eAVEncVideoColorTransferMatrix_BT601, codecapi/eAVEncVideoColorTransferMatrix_BT709, codecapi/eAVEncVideoColorTransferMatrix_SMPTE240M, codecapi/eAVEncVideoColorTransferMatrix_SameAsSource, dshow.eavencvideocolortransfermatrix, eAVEncVideoColorTransferMatrix, eAVEncVideoColorTransferMatrix enumeration [DirectShow], eAVEncVideoColorTransferMatrixEnumeration, eAVEncVideoColorTransferMatrix_BT601, eAVEncVideoColorTransferMatrix_BT709, eAVEncVideoColorTransferMatrix_SMPTE240M, eAVEncVideoColorTransferMatrix_SameAsSource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorTransferMatrix
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVEncVideoColorTransferMatrix enumeration


## -description



Specifies the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space. This enumeration is used with the <a href="https://msdn.microsoft.com/de03f3e6-12c8-4a7c-a424-ef974d223e70">AVEncVideoInputColorTransferMatrix</a> and <a href="https://msdn.microsoft.com/48891204-397b-4b2b-8550-7a77461db06c">AVEncVideoOutputColorTransferMatrix</a> properties.




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




<a href="https://msdn.microsoft.com/en-us/library/Dd387884(v=VS.85).aspx">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 


---
UID: NE:dxva2api._DXVA2_VideoTransferMatrix
title: DXVA2_VideoTransferMatrix (dxva2api.h)
author: windows-sdk-content
description: Describes the conversion matrices between Y'PbPr (component video) and studio R'G'B'.
old-location: mf\dxva2_videotransfermatrix.htm
tech.root: medfound
ms.assetid: 682fa0c7-8f17-457f-9f8a-dc9190866152
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 682fa0c7-8f17-457f-9f8a-dc9190866152, DXVA2_VideoTransferMatrix, DXVA2_VideoTransferMatrix enumeration [Media Foundation], DXVA2_VideoTransferMatrixMask, DXVA2_VideoTransferMatrix_BT601, DXVA2_VideoTransferMatrix_BT709, DXVA2_VideoTransferMatrix_SMPTE240M, DXVA2_VideoTransferMatrix_Unknown, dxva2api/DXVA2_VideoTransferMatrix, dxva2api/DXVA2_VideoTransferMatrixMask, dxva2api/DXVA2_VideoTransferMatrix_BT601, dxva2api/DXVA2_VideoTransferMatrix_BT709, dxva2api/DXVA2_VideoTransferMatrix_SMPTE240M, dxva2api/DXVA2_VideoTransferMatrix_Unknown, mf.dxva2_videotransfermatrix
ms.topic: enum
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - dxva2api.h
api_name:
 - DXVA2_VideoTransferMatrix
product: Windows
targetos: Windows
req.typenames: DXVA2_VideoTransferMatrix
req.redist: 
---

# DXVA2_VideoTransferMatrix enumeration


## -description


Describes the conversion matrices between Y'PbPr (component video) and studio R'G'B'. These flags are used in the <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure.


## -enum-fields




### -field DXVA2_VideoTransferMatrixMask

Bitmask to validate flag values. This value is not a valid flag.
          


### -field DXVA2_VideoTransferMatrix_Unknown

Unknown. For standard-definition content, treat as DXVA2_VideoTransferMatrix_BT601. For high-definition content, treat as DXVA2_VideoTransferMatrix_BT709. (High-definition content is defined for this purpose as anything with a source height greater than 576 lines.)
          


### -field DXVA2_VideoTransferMatrix_BT709

ITU-R BT.709 transfer matrix.
          


### -field DXVA2_VideoTransferMatrix_BT601

ITU-R BT.601 transfer matrix. Also used for SMPTE 170 and ITU-R BT.470-2 System B,G.
          


### -field DXVA2_VideoTransferMatrix_SMPTE240M

SMPTE 240M transfer matrix.
          


## -remarks



The transfer matrices are defined as follows.

BT.709 transfer matrices:

<pre class="syntax" xml:space="preserve"><code>Y'        0.212600    0.715200    0.072200       R' 
Pb   =   -0.114572   -0.385428    0.500000   x   G' 
Pr        0.500000   -0.454153   -0.045847       B' 

R'        1.000000    0.000000    1.574800       Y' 
G'   =    1.000000   -0.187324   -0.468124   x   Pb 
B'        1.000000    1.855600    0.000000       Pr 
</code></pre>
BT.601 transfer matrices:

<pre class="syntax" xml:space="preserve"><code>Y'        0.299000    0.587000    0.114000       R' 
Pb   =   -0.168736   -0.331264    0.500000   x   G' 
Pr        0.500000   -0.418688   -0.081312       B' 

R'        1.000000    0.000000    1.402000       Y' 
G'   =    1.000000   -0.344136   -0.714136   x   Pb 
B'        1.000000    1.772000    0.000000       Pr 
</code></pre>
SMPTE 240M (SMPTE RP 145) transfer matrices:

<pre class="syntax" xml:space="preserve"><code>Y'        0.212000    0.701000    0.087000       R' 
Pb   =   -0.116000   -0.384000    0.500000   x   G' 
Pr        0.500000   -0.445000   -0.055000       B' 

R'        1.000000   -0.000000    1.576000       Y' 
G'   =    1.000000   -0.227000   -0.477000   x   Pb 
B'        1.000000    1.826000    0.000000       Pr 
</code></pre>
This enumeration is equivalent to the <b>DXVA_VideoTransferMatrix</b> enumeration used in DXVA 1.0.

If you are using the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface to describe the video format, the video transfer matrix is specified in the <a href="https://msdn.microsoft.com/b268d16d-b4cc-4026-9ba7-805cc5409b95">MF_MT_YUV_MATRIX</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


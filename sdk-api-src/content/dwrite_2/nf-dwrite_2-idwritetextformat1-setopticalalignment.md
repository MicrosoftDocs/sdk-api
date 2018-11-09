---
UID: NF:dwrite_2.IDWriteTextFormat1.SetOpticalAlignment
title: IDWriteTextFormat1::SetOpticalAlignment
author: windows-sdk-content
description: Sets the optical margin alignment for the text format.
old-location: directwrite\idwritetextformat1_setopticalalignment.htm
tech.root: DirectWrite
ms.assetid: FA050DAC-2788-4159-B299-D4B6100D85F4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDWriteTextFormat1 interface [Direct Write],SetOpticalAlignment method, IDWriteTextFormat1.SetOpticalAlignment, IDWriteTextFormat1::SetOpticalAlignment, SetOpticalAlignment, SetOpticalAlignment method [Direct Write], SetOpticalAlignment method [Direct Write],IDWriteTextFormat1 interface, directwrite.idwritetextformat1_setopticalalignment, dwrite_2/IDWriteTextFormat1::SetOpticalAlignment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextFormat1.SetOpticalAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextFormat1::SetOpticalAlignment


## -description


Sets the optical margin alignment for the text format.

By default, glyphs are aligned to the margin by the default origin and side-bearings of the glyph. If you specify <b>DWRITE_OPTICAL_ALIGNMENT_USING_SIDE_BEARINGS</b>, then the alignment Suses the side bearings to offset the glyph from the aligned edge to ensure the ink of the glyphs are aligned.
      


## -parameters




### -param opticalAlignment

The optical alignment to set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/15295A17-E542-4071-AE38-02014A1235D5">IDWriteTextFormat1</a>
 

 


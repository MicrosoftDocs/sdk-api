---
UID: NF:vidcap.IVideoProcAmp.put_Contrast
title: IVideoProcAmp::put_Contrast (vidcap.h)
description: The put_Contrast method sets the camera's contrast setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_Contrast method","IVideoProcAmp.put_Contrast","IVideoProcAmp::put_Contrast","IVideoProcAmpput_Contrast","dshow.ivideoprocamp_put_contrast","put_Contrast","put_Contrast method [DirectShow]","put_Contrast method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_Contrast"]
old-location: dshow\ivideoprocamp_put_contrast.htm
tech.root: dshow
ms.assetid: a03ab735-2258-49c6-a66a-fabe38f88532
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_Contrast method, IVideoProcAmp.put_Contrast, IVideoProcAmp::put_Contrast, IVideoProcAmpput_Contrast, dshow.ivideoprocamp_put_contrast, put_Contrast, put_Contrast method [DirectShow], put_Contrast method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Contrast
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVideoProcAmp::put_Contrast
 - vidcap/IVideoProcAmp::put_Contrast
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.put_Contrast
---

# IVideoProcAmp::put_Contrast


## -description

The <code>put_Contrast</code> method sets the camera's contrast setting.

## -parameters

### -param Value [in]

Specifies the contrast setting. Larger values indicate increased contrast.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
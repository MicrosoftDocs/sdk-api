---
UID: NF:vidcap.IVideoProcAmp.get_Contrast
title: IVideoProcAmp::get_Contrast (vidcap.h)
description: The get_Contrast method returns the camera's contrast setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_Contrast method","IVideoProcAmp.get_Contrast","IVideoProcAmp::get_Contrast","IVideoProcAmpget_Contrast","dshow.ivideoprocamp_get_contrast","get_Contrast","get_Contrast method [DirectShow]","get_Contrast method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_Contrast"]
old-location: dshow\ivideoprocamp_get_contrast.htm
tech.root: dshow
ms.assetid: 04c63013-33f1-42c0-9239-ec012c9a0528
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Contrast method, IVideoProcAmp.get_Contrast, IVideoProcAmp::get_Contrast, IVideoProcAmpget_Contrast, dshow.ivideoprocamp_get_contrast, get_Contrast, get_Contrast method [DirectShow], get_Contrast method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Contrast
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
 - IVideoProcAmp::get_Contrast
 - vidcap/IVideoProcAmp::get_Contrast
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
 - IVideoProcAmp.get_Contrast
---

# IVideoProcAmp::get_Contrast


## -description

The <code>get_Contrast</code> method returns the camera's contrast setting.

## -parameters

### -param pValue [out]

Receives the contrast setting. Larger values indicate increased contrast.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
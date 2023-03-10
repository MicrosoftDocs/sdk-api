---
UID: NF:vidcap.IVideoProcAmp.get_Saturation
title: IVideoProcAmp::get_Saturation (vidcap.h)
description: The get_Saturation method returns the camera's saturation setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_Saturation method","IVideoProcAmp.get_Saturation","IVideoProcAmp::get_Saturation","IVideoProcAmpget_Saturation","dshow.ivideoprocamp_get_saturation","get_Saturation","get_Saturation method [DirectShow]","get_Saturation method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_Saturation"]
old-location: dshow\ivideoprocamp_get_saturation.htm
tech.root: dshow
ms.assetid: 977e71a4-8118-4fc2-9f76-ec30293b33d0
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_Saturation method, IVideoProcAmp.get_Saturation, IVideoProcAmp::get_Saturation, IVideoProcAmpget_Saturation, dshow.ivideoprocamp_get_saturation, get_Saturation, get_Saturation method [DirectShow], get_Saturation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Saturation
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
 - IVideoProcAmp::get_Saturation
 - vidcap/IVideoProcAmp::get_Saturation
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
 - IVideoProcAmp.get_Saturation
---

# IVideoProcAmp::get_Saturation


## -description

The <code>get_Saturation</code> method returns the camera's saturation setting.

## -parameters

### -param pValue [out]

Receives the saturation setting. Larger values indicate greater saturation. The value zero indicates grayscale.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
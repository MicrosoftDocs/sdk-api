---
UID: NF:vidcap.IVideoProcAmp.put_Gain
title: IVideoProcAmp::put_Gain (vidcap.h)
description: The put_Gain method sets the camera's gain setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_Gain method","IVideoProcAmp.put_Gain","IVideoProcAmp::put_Gain","IVideoProcAmpput_Gain","dshow.ivideoprocamp_put_gain","put_Gain","put_Gain method [DirectShow]","put_Gain method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_Gain"]
old-location: dshow\ivideoprocamp_put_gain.htm
tech.root: dshow
ms.assetid: 8256c1d9-ca3f-4b6a-921d-a424932927b5
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_Gain method, IVideoProcAmp.put_Gain, IVideoProcAmp::put_Gain, IVideoProcAmpput_Gain, dshow.ivideoprocamp_put_gain, put_Gain, put_Gain method [DirectShow], put_Gain method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Gain
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
 - IVideoProcAmp::put_Gain
 - vidcap/IVideoProcAmp::put_Gain
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
 - IVideoProcAmp.put_Gain
---

# IVideoProcAmp::put_Gain


## -description

The <code>put_Gain</code> method sets the camera's gain setting.

## -parameters

### -param Value [in]

Specifies the gain setting. Larger values indicate higher gain.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
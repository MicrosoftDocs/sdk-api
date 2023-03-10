---
UID: NF:vidcap.IVideoProcAmp.put_Brightness
title: IVideoProcAmp::put_Brightness (vidcap.h)
description: The put_Brightness method sets the camera's brightness setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_Brightness method","IVideoProcAmp.put_Brightness","IVideoProcAmp::put_Brightness","IVideoProcAmpput_Brightness","dshow.ivideoprocamp_put_brightness","put_Brightness","put_Brightness method [DirectShow]","put_Brightness method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_Brightness"]
old-location: dshow\ivideoprocamp_put_brightness.htm
tech.root: dshow
ms.assetid: 69c8086c-a638-4ec6-a4fd-5a400095145d
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],put_Brightness method, IVideoProcAmp.put_Brightness, IVideoProcAmp::put_Brightness, IVideoProcAmpput_Brightness, dshow.ivideoprocamp_put_brightness, put_Brightness, put_Brightness method [DirectShow], put_Brightness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Brightness
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
 - IVideoProcAmp::put_Brightness
 - vidcap/IVideoProcAmp::put_Brightness
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
 - IVideoProcAmp.put_Brightness
---

# IVideoProcAmp::put_Brightness


## -description

The <code>put_Brightness</code> method sets the camera's brightness setting.

## -parameters

### -param Value [in]

Specifies the brightness setting. Larger values indicate increased brightness.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
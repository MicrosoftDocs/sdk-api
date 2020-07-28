---
UID: NF:vidcap.IVideoProcAmp.get_BacklightCompensation
title: IVideoProcAmp::get_BacklightCompensation (vidcap.h)
description: The get_BacklightCompensation method returns the camera's backlight compensation setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_BacklightCompensation method","IVideoProcAmp.get_BacklightCompensation","IVideoProcAmp::get_BacklightCompensation","IVideoProcAmpget_BacklightCompensation","dshow.ivideoprocamp_get_backlightcompensation","get_BacklightCompensation","get_BacklightCompensation method [DirectShow]","get_BacklightCompensation method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_BacklightCompensation"]
old-location: dshow\ivideoprocamp_get_backlightcompensation.htm
tech.root: dshow
ms.assetid: 1b0b4c06-5958-446e-bd06-4ee6f90b6e78
ms.date: 12/05/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_BacklightCompensation method, IVideoProcAmp.get_BacklightCompensation, IVideoProcAmp::get_BacklightCompensation, IVideoProcAmpget_BacklightCompensation, dshow.ivideoprocamp_get_backlightcompensation, get_BacklightCompensation, get_BacklightCompensation method [DirectShow], get_BacklightCompensation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_BacklightCompensation
f1_keywords:
- vidcap/IVideoProcAmp.get_BacklightCompensation
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Vidcap.h
api_name:
- IVideoProcAmp.get_BacklightCompensation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVideoProcAmp::get_BacklightCompensation


## -description


The <code>get_BacklightCompensation</code> method returns the camera's backlight compensation setting.


## -parameters




### -param pValue [out]

Receives the backlight compensation setting. If the value is zero, backlight compensation is disabled. Otherwise, backlight compensation is enabled. The camera may support a Boolean setting (0/1) or a range of settings. If it supports a range of settings, higher numbers indicate a greater degree of backlight compensation.


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>
 

 


---
UID: NF:tuner.IAnalogAudioComponentType.get_AnalogAudioMode
title: IAnalogAudioComponentType::get_AnalogAudioMode (tuner.h)
description: The get_AnalogAudioMode method retrieves the analog audio mode.
helpviewer_keywords: ["IAnalogAudioComponentType interface [Microsoft TV Technologies]","get_AnalogAudioMode method","IAnalogAudioComponentType.get_AnalogAudioMode","IAnalogAudioComponentType::get_AnalogAudioMode","IAnalogAudioComponentTypeget_AnalogAudioMode","get_AnalogAudioMode","get_AnalogAudioMode method [Microsoft TV Technologies]","get_AnalogAudioMode method [Microsoft TV Technologies]","IAnalogAudioComponentType interface","mstv.ianalogaudiocomponenttype_get_analogaudiomode","tuner/IAnalogAudioComponentType::get_AnalogAudioMode"]
old-location: mstv\ianalogaudiocomponenttype_get_analogaudiomode.htm
tech.root: mstv
ms.assetid: 63c5f2a0-5524-4df0-bc0d-fcd7c6b36167
ms.date: 12/05/2018
ms.keywords: IAnalogAudioComponentType interface [Microsoft TV Technologies],get_AnalogAudioMode method, IAnalogAudioComponentType.get_AnalogAudioMode, IAnalogAudioComponentType::get_AnalogAudioMode, IAnalogAudioComponentTypeget_AnalogAudioMode, get_AnalogAudioMode, get_AnalogAudioMode method [Microsoft TV Technologies], get_AnalogAudioMode method [Microsoft TV Technologies],IAnalogAudioComponentType interface, mstv.ianalogaudiocomponenttype_get_analogaudiomode, tuner/IAnalogAudioComponentType::get_AnalogAudioMode
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - IAnalogAudioComponentType::get_AnalogAudioMode
 - tuner/IAnalogAudioComponentType::get_AnalogAudioMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IAnalogAudioComponentType.get_AnalogAudioMode
---

# IAnalogAudioComponentType::get_AnalogAudioMode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_AnalogAudioMode</b> method retrieves the analog audio mode.

## -parameters

### -param Mode [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-tvaudiomode">TVAudioMode</a> variable that receives the analog audio mode.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogaudiocomponenttype">IAnalogAudioComponentType Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogaudiocomponenttype-put_analogaudiomode">put_AnalogAudioMode</a>
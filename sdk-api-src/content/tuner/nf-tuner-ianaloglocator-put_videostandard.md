---
UID: NF:tuner.IAnalogLocator.put_VideoStandard
title: IAnalogLocator::put_VideoStandard (tuner.h)
description: The put_VideoStandard method specifies the format of the analog television signal.
helpviewer_keywords: ["IAnalogLocator interface [Microsoft TV Technologies]","put_VideoStandard method","IAnalogLocator.put_VideoStandard","IAnalogLocator::put_VideoStandard","IAnalogLocatorput_VideoStandard","mstv.ianaloglocator_put_videostandard","put_VideoStandard","put_VideoStandard method [Microsoft TV Technologies]","put_VideoStandard method [Microsoft TV Technologies]","IAnalogLocator interface","tuner/IAnalogLocator::put_VideoStandard"]
old-location: mstv\ianaloglocator_put_videostandard.htm
tech.root: mstv
ms.assetid: 6af47a98-ceea-45dd-8a34-3f82ed8a66b1
ms.date: 12/05/2018
ms.keywords: IAnalogLocator interface [Microsoft TV Technologies],put_VideoStandard method, IAnalogLocator.put_VideoStandard, IAnalogLocator::put_VideoStandard, IAnalogLocatorput_VideoStandard, mstv.ianaloglocator_put_videostandard, put_VideoStandard, put_VideoStandard method [Microsoft TV Technologies], put_VideoStandard method [Microsoft TV Technologies],IAnalogLocator interface, tuner/IAnalogLocator::put_VideoStandard
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
 - IAnalogLocator::put_VideoStandard
 - tuner/IAnalogLocator::put_VideoStandard
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
 - IAnalogLocator.put_VideoStandard
---

# IAnalogLocator::put_VideoStandard


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_VideoStandard</b> method specifies the format of the analog television signal.

## -parameters

### -param AVS [in]

Specifies the format of the analog television signal. This parameter is of type <a href="/windows/win32/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard</a>.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved by using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ianaloglocator">IAnalogLocator Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ianaloglocator-get_videostandard">get_VideoStandard</a>
---
UID: NN:strmif.IAMTuner
title: IAMTuner (strmif.h)
description: The IAMTuner interface controls a TV tuner.
helpviewer_keywords: ["IAMTuner","IAMTuner interface [DirectShow]","IAMTuner interface [DirectShow]","described","IAMTunerInterface","dshow.iamtuner","strmif/IAMTuner"]
old-location: dshow\iamtuner.htm
tech.root: dshow
ms.assetid: 997d39c5-a1a5-4d2d-8704-9846f149712c
ms.date: 12/05/2018
ms.keywords: IAMTuner, IAMTuner interface [DirectShow], IAMTuner interface [DirectShow],described, IAMTunerInterface, dshow.iamtuner, strmif/IAMTuner
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTuner
 - strmif/IAMTuner
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner
---

# IAMTuner interface


## -description

The <code>IAMTuner</code> interface controls a TV tuner. This interface is the base class for the <a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner</a> interface, which inherits all of the <code>IAMTuner</code> methods. For more information on controlling a TV tuner using Microsoft DirectShow, see the <b>IAMTVTuner</b> documentation.

## -inheritance

The <b>IAMTuner</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTuner</b> also has these types of members:


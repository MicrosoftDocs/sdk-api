---
UID: NN:tuner.ITuner
title: ITuner (tuner.h)
description: The ITuner interface is implemented on the Microsoft BDA Network Provider filters.
helpviewer_keywords: ["ITuner","ITuner interface [Microsoft TV Technologies]","ITuner interface [Microsoft TV Technologies]","described","ITunerInterface","mstv.ituner","tuner/ITuner"]
old-location: mstv\ituner.htm
tech.root: mstv
ms.assetid: 1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd
ms.date: 12/05/2018
ms.keywords: ITuner, ITuner interface [Microsoft TV Technologies], ITuner interface [Microsoft TV Technologies],described, ITunerInterface, mstv.ituner, tuner/ITuner
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ITuner
 - tuner/ITuner
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
 - ITuner
---

# ITuner interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ITuner</b> interface is implemented on the Microsoft <a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a> filters. It provides methods for passing tune requests down to the hardware device and receiving current tuning settings. Generally, applications should use the derived interface <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a> instead of <b>ITuner</b>.

<div class="alert"><b>Note</b>  Only applications that are intended to run on Windows 2000 should use this interface. Starting in Windows XP, the Video Control handles all tuning interactions with the Network Provider.</div>
<div> </div>

## -inheritance

The <b>ITuner</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITuner</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuner)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>

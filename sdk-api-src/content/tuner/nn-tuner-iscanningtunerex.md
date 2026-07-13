---
UID: NN:tuner.IScanningTunerEx
title: IScanningTunerEx (tuner.h)
description: This topic applies to Windows Vista.
helpviewer_keywords: ["IScanningTunerEx","IScanningTunerEx interface [Microsoft TV Technologies]","IScanningTunerEx interface [Microsoft TV Technologies]","described","IScanningTunerExInterface","mstv.iscanningtunerex","tuner/IScanningTunerEx"]
old-location: mstv\iscanningtunerex.htm
tech.root: mstv
ms.assetid: 3f89173a-d24b-400c-a229-28efb7a703be
ms.date: 12/05/2018
ms.keywords: IScanningTunerEx, IScanningTunerEx interface [Microsoft TV Technologies], IScanningTunerEx interface [Microsoft TV Technologies],described, IScanningTunerExInterface, mstv.iscanningtunerex, tuner/IScanningTunerEx
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
 - IScanningTunerEx
 - tuner/IScanningTunerEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tuner.h
api_name:
 - IScanningTunerEx
---

# IScanningTunerEx interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows Vista.
        

The <b>IScanningTunerEx</b> interface is an extended version of <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a> and is exposed by the <a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a> filter. It inherits from <b>IScanningTuner</b> and permits direct control of a tuner that supports searching for valid programming. The client must provide a valid tuning space (using <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tuningspace">ITuner::put_TuningSpace</a> or <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tunerequest">ITuner::put_TuneRequest</a>) before calling any of the methods in this interface. This interface is meant to be used in conjunction with the <a href="/previous-versions/dd376294(v=vs.85)">IBroadcastEvent</a> outbound interface.

## -inheritance

The <b>IScanningTunerEx</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a>. <b>IScanningTunerEx</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IScanningTunerEx)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a>

---
UID: NN:tuner.IScanningTuner
title: IScanningTuner (tuner.h)
description: The IScanningTuner interface is implemented on the BDA Network Provider filter.
helpviewer_keywords: ["IScanningTuner","IScanningTuner interface [Microsoft TV Technologies]","IScanningTuner interface [Microsoft TV Technologies]","described","IScanningTunerInterface","mstv.iscanningtuner","tuner/IScanningTuner"]
old-location: mstv\iscanningtuner.htm
tech.root: mstv
ms.assetid: faa99b87-ddbb-4e38-8681-bd5c8c4f81f3
ms.date: 12/05/2018
ms.keywords: IScanningTuner, IScanningTuner interface [Microsoft TV Technologies], IScanningTuner interface [Microsoft TV Technologies],described, IScanningTunerInterface, mstv.iscanningtuner, tuner/IScanningTuner
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
 - IScanningTuner
 - tuner/IScanningTuner
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
 - IScanningTuner
---

# IScanningTuner interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IScanningTuner</b> interface is implemented on the <a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a> filter. It inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner</a> and permits direct control of a tuner that supports searching for valid programming. The client must provide a valid tuning space (using <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tuningspace">ITuner::put_TuningSpace</a> or <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituner-put_tunerequest">ITuner::put_TuneRequest</a>) before calling any of the methods in this interface. This interface is meant to be used in conjunction with the <a href="/previous-versions/dd376294(v=vs.85)">IBroadcastEvent</a> outbound interface.

<div class="alert"><b>Note</b>  Only applications intended to run on Microsoft® Windows® 98 or Windows 2000 should use this interface. On Windows XP, the Video Control handles all tuning interactions with the Network Provider.</div>
<div> </div>

## -inheritance

The <b>IScanningTuner</b> interface inherits from <a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">ITuner</a>. <b>IScanningTuner</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Currently the DVB-C and DVB-S Network Provider filters do not implement this interface. The interface is implemented for DVB-T.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IScanningTuner)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>



<a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">ITuner</a>

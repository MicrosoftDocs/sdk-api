---
UID: NF:msvidctl.IMSVidCtl.get_FeaturesAvailable
title: IMSVidCtl::get_FeaturesAvailable (msvidctl.h)
description: The get_FeaturesAvailable method retrieves the features that are available on the local system.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_FeaturesAvailable method","IMSVidCtl.get_FeaturesAvailable","IMSVidCtl::get_FeaturesAvailable","IMSVidCtlget_FeaturesAvailable","get_FeaturesAvailable","get_FeaturesAvailable method [Microsoft TV Technologies]","get_FeaturesAvailable method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_featuresavailable","msvidctl/IMSVidCtl::get_FeaturesAvailable"]
old-location: mstv\imsvidctl_get_featuresavailable.htm
tech.root: mstv
ms.assetid: 73da686c-0c25-4dfb-8a13-681f1dac6a4a
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_FeaturesAvailable method, IMSVidCtl.get_FeaturesAvailable, IMSVidCtl::get_FeaturesAvailable, IMSVidCtlget_FeaturesAvailable, get_FeaturesAvailable, get_FeaturesAvailable method [Microsoft TV Technologies], get_FeaturesAvailable method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_featuresavailable, msvidctl/IMSVidCtl::get_FeaturesAvailable
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - IMSVidCtl::get_FeaturesAvailable
 - msvidctl/IMSVidCtl::get_FeaturesAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.get_FeaturesAvailable
---

# IMSVidCtl::get_FeaturesAvailable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_FeaturesAvailable</b> method retrieves the features that are available on the local system.

## -parameters

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidfeatures">IMSVidFeatures</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method returns a collection of feature objects. Use the returned <a href="/previous-versions/windows/desktop/mstv/msvidfeatures">IMSVidFeatures</a> pointer to enumerate the collection. To activate a feature, add it to the active features collection. To search for a specific feature, call the <a href="/windows/desktop/api/segment/nf-segment-imsviddevice-get__classid">IMSVidDevice::get__ClassID</a> method on each feature and compare the result against the CLSID of the feature you are looking for.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>
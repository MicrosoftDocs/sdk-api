---
UID: NF:msvidctl.IMSVidCtl.put_FeaturesActive
title: IMSVidCtl::put_FeaturesActive (msvidctl.h)
description: The put_FeaturesActive method specifies a collection of features to activate.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_FeaturesActive method","IMSVidCtl.put_FeaturesActive","IMSVidCtl::put_FeaturesActive","IMSVidCtlput_FeaturesActive","mstv.imsvidctl_put_featuresactive","msvidctl/IMSVidCtl::put_FeaturesActive","put_FeaturesActive","put_FeaturesActive method [Microsoft TV Technologies]","put_FeaturesActive method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_featuresactive.htm
tech.root: mstv
ms.assetid: 293506fa-3208-468e-982a-3c1f8ce0269b
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_FeaturesActive method, IMSVidCtl.put_FeaturesActive, IMSVidCtl::put_FeaturesActive, IMSVidCtlput_FeaturesActive, mstv.imsvidctl_put_featuresactive, msvidctl/IMSVidCtl::put_FeaturesActive, put_FeaturesActive, put_FeaturesActive method [Microsoft TV Technologies], put_FeaturesActive method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_FeaturesActive
 - msvidctl/IMSVidCtl::put_FeaturesActive
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
 - IMSVidCtl.put_FeaturesActive
---

# IMSVidCtl::put_FeaturesActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_FeaturesActive</b> method specifies a collection of features to activate.

## -parameters

### -param pVal [in]

Pointer to the <a href="/previous-versions/windows/desktop/mstv/msvidfeatures">IMSVidFeatures</a> interface on a collection of features.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Features represent additional capabilities beyond basic tuning and rendering, such as closed captioning or IP data services. When the Video Control builds the filter graph, it uses the active features collection to configure the graph.

For a default graph, it is not necessary to specify the active features. To activate a feature, create a new <a href="/previous-versions/windows/desktop/legacy/dd695126(v=vs.85)">MSVidFeatures</a> collection object. Then use the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_featuresavailable">IMSVidCtl::get_FeaturesAvailable</a> method to enumerate the available features, and call <a href="/windows/desktop/api/segment/nf-segment-imsviddevice-get__classid">IMSVidDevice::get__ClassID</a> on each feature. If the CLSID matches the feature you wish to activate, add that feature to your MSVidFeatures collection. Then call <b>put_FeaturesActive</b> with a pointer to the MSVidFeatures collection.

If the Video Control's state is not <b>STATE_UNBUILT</b>, call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-decompose">IMSVidCtl::Decompose</a> to tear down the filter graph before calling this method.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_featuresactive">IMSVidCtl::get_FeaturesActive</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_state">IMSVidCtl::get_State</a>
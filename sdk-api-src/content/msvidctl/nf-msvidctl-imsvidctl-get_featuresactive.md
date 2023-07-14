---
UID: NF:msvidctl.IMSVidCtl.get_FeaturesActive
title: IMSVidCtl::get_FeaturesActive (msvidctl.h)
description: The get_FeaturesActive method retrieves the features that are currently active.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_FeaturesActive method","IMSVidCtl.get_FeaturesActive","IMSVidCtl::get_FeaturesActive","IMSVidCtlget_FeaturesActive","get_FeaturesActive","get_FeaturesActive method [Microsoft TV Technologies]","get_FeaturesActive method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_featuresactive","msvidctl/IMSVidCtl::get_FeaturesActive"]
old-location: mstv\imsvidctl_get_featuresactive.htm
tech.root: mstv
ms.assetid: 33832fe2-e8ef-4e37-9af9-90f566feb559
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_FeaturesActive method, IMSVidCtl.get_FeaturesActive, IMSVidCtl::get_FeaturesActive, IMSVidCtlget_FeaturesActive, get_FeaturesActive, get_FeaturesActive method [Microsoft TV Technologies], get_FeaturesActive method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_featuresactive, msvidctl/IMSVidCtl::get_FeaturesActive
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
 - IMSVidCtl::get_FeaturesActive
 - msvidctl/IMSVidCtl::get_FeaturesActive
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
 - IMSVidCtl.get_FeaturesActive
---

# IMSVidCtl::get_FeaturesActive


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_FeaturesActive</b> method retrieves the features that are currently active.

## -parameters

### -param pVal [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidfeatures">IMSVidFeatures</a> interface pointer. The caller must release the interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If no features are active, the method might return <b>NULL</b> in the <i>pVal</i> parameter. Otherwise, it returns a collection of feature objects. Use the returned <a href="/previous-versions/windows/desktop/mstv/msvidfeatures">IMSVidFeatures</a> pointer to enumerate the collection.


#### Examples


```cpp

CComPtr<IMSVidFeatures> pFeatures;
hr = m_pVideoControl->get_FeaturesActive(&pFeatures);
if (SUCCEEDED(hr) && pFeatures)
{
    long c;
    pFs->get_Count(&c);
    /* Enumerate the features */
}

```

## -see-also

<a href="/previous-versions/windows/desktop/mstv/displaying-closed-captioning-in-c">Displaying Closed Captioning in C++</a>



<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_featuresactive">IMSVidCtl::put_FeaturesActive</a>
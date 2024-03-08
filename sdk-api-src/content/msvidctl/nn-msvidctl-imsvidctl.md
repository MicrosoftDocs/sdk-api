---
UID: NN:msvidctl.IMSVidCtl
title: IMSVidCtl (msvidctl.h)
description: The IMSVidCtl interface is the main interface for the Video Control.
helpviewer_keywords: ["IMSVidCtl","IMSVidCtl interface [Microsoft TV Technologies]","IMSVidCtl interface [Microsoft TV Technologies]","described","IMSVidCtlInterface","mstv.imsvidctl","msvidctl/IMSVidCtl"]
old-location: mstv\imsvidctl.htm
tech.root: mstv
ms.assetid: e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee
ms.date: 12/05/2018
ms.keywords: IMSVidCtl, IMSVidCtl interface [Microsoft TV Technologies], IMSVidCtl interface [Microsoft TV Technologies],described, IMSVidCtlInterface, mstv.imsvidctl, msvidctl/IMSVidCtl
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
 - IMSVidCtl
 - msvidctl/IMSVidCtl
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
 - IMSVidCtl
---

# IMSVidCtl interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidCtl</b> interface is the main interface for the <a href="/previous-versions/windows/desktop/legacy/ee663618(v=vs.85)">Video Control</a>. It contains methods to enumerate available devices and features, and to select which features and devices will be active. It also contains methods to build, stop, start, and pause the filter graph.

## -inheritance

The <b>IMSVidCtl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMSVidCtl</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidCtl)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/using-the-video-control">Using the Video Control</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>

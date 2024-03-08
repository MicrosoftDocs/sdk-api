---
UID: NN:tuner.IESLicenseRenewalResultEvent
title: IESLicenseRenewalResultEvent (tuner.h)
description: Implements methods that get information from a LicenseRenewalResult event.
helpviewer_keywords: ["IESLicenseRenewalResultEvent","IESLicenseRenewalResultEvent interface [DirectShow]","IESLicenseRenewalResultEvent interface [DirectShow]","described","mstv.ieslicenserenewalresultevent","tuner/IESLicenseRenewalResultEvent"]
old-location: mstv\ieslicenserenewalresultevent.htm
tech.root: mstv
ms.assetid: 6f9cbec4-7934-41fc-b387-3f45aa273a72
ms.date: 12/05/2018
ms.keywords: IESLicenseRenewalResultEvent, IESLicenseRenewalResultEvent interface [DirectShow], IESLicenseRenewalResultEvent interface [DirectShow],described, mstv.ieslicenserenewalresultevent, tuner/IESLicenseRenewalResultEvent
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IESLicenseRenewalResultEvent
 - tuner/IESLicenseRenewalResultEvent
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
 - IESLicenseRenewalResultEvent
---

# IESLicenseRenewalResultEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get information from a  <b>LicenseRenewalResult</b> event. This event contains the results of an attempt to renew a license for protected content. If the attempt succeeds, the results contain the license; if the attempt fails, the results contain error information.

## -inheritance

The <b>IESLicenseRenewalResultEvent</b> interface inherits from <b>IESEvent</b>. <b>IESLicenseRenewalResultEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESLicenseRenewalResultEvent)</code>.

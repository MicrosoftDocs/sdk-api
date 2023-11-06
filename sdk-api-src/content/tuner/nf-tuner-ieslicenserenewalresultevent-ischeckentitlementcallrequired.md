---
UID: NF:tuner.IESLicenseRenewalResultEvent.IsCheckEntitlementCallRequired
title: IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired (tuner.h)
description: Gets a flag from a LicenseRenewalResult event that indicates whether the client should check the entitlement token from the license. The client can call the IBDA_ConditionalAccessEx::CheckEntitlementToken method to validate the entitlement token.
helpviewer_keywords: ["IESLicenseRenewalResultEvent interface [DirectShow]","IsCheckEntitlementCallRequired method","IESLicenseRenewalResultEvent.IsCheckEntitlementCallRequired","IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired","IsCheckEntitlementCallRequired","IsCheckEntitlementCallRequired method [DirectShow]","IsCheckEntitlementCallRequired method [DirectShow]","IESLicenseRenewalResultEvent interface","mstv.ieslicenserenewalresultevent_ischeckentitlementcallrequired","tuner/IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired"]
old-location: mstv\ieslicenserenewalresultevent_ischeckentitlementcallrequired.htm
tech.root: mstv
ms.assetid: e19375c6-5999-43e9-9d91-3237b900cb07
ms.date: 12/05/2018
ms.keywords: IESLicenseRenewalResultEvent interface [DirectShow],IsCheckEntitlementCallRequired method, IESLicenseRenewalResultEvent.IsCheckEntitlementCallRequired, IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired, IsCheckEntitlementCallRequired, IsCheckEntitlementCallRequired method [DirectShow], IsCheckEntitlementCallRequired method [DirectShow],IESLicenseRenewalResultEvent interface, mstv.ieslicenserenewalresultevent_ischeckentitlementcallrequired, tuner/IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired
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
 - IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired
 - tuner/IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired
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
 - IESLicenseRenewalResultEvent.IsCheckEntitlementCallRequired
---

# IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets a flag from a <b>LicenseRenewalResult</b> event that indicates whether the client should check the entitlement token from the license. The client can call the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccessex-checkentitlementtoken">IBDA_ConditionalAccessEx::CheckEntitlementToken</a> method to validate the entitlement token.

## -parameters

### -param pfCheckEntTokenCallNeeded [out, retval]

Receives the check entitlement token flag: 1 indicates that a check is needed; 0 indicates that no check is needed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccessex-checkentitlementtoken">IBDA_ConditionalAccessEx::CheckEntitlementToken</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>
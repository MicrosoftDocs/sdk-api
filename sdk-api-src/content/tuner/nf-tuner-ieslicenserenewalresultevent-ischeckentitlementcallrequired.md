---
UID: NF:tuner.IESLicenseRenewalResultEvent.IsCheckEntitlementCallRequired
title: IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired
author: windows-sdk-content
description: Gets a flag from a LicenseRenewalResult event that indicates whether the client should check the entitlement token from the license. The client can call the IBDA_ConditionalAccessEx::CheckEntitlementToken method to validate the entitlement token.
old-location: mstv\ieslicenserenewalresultevent_ischeckentitlementcallrequired.htm
tech.root: mstv
ms.assetid: e19375c6-5999-43e9-9d91-3237b900cb07
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IESLicenseRenewalResultEvent interface [DirectShow],IsCheckEntitlementCallRequired method, IESLicenseRenewalResultEvent.IsCheckEntitlementCallRequired, IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired, IsCheckEntitlementCallRequired, IsCheckEntitlementCallRequired method [DirectShow], IsCheckEntitlementCallRequired method [DirectShow],IESLicenseRenewalResultEvent interface, mstv.ieslicenserenewalresultevent_ischeckentitlementcallrequired, tuner/IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESLicenseRenewalResultEvent.IsCheckEntitlementCallRequired
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESLicenseRenewalResultEvent::IsCheckEntitlementCallRequired


## -description


 Gets a flag from a <b>LicenseRenewalResult</b> event that indicates whether the client should check the entitlement token from the license. The client can call the <a href="https://msdn.microsoft.com/ea581065-b10b-4a2a-9090-99d6fd140ea9">IBDA_ConditionalAccessEx::CheckEntitlementToken</a> method to validate the entitlement token.


## -parameters




### -param pfCheckEntTokenCallNeeded [out, retval]

Receives the check entitlement token flag: 1 indicates that a check is needed; 0 indicates that no check is needed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ea581065-b10b-4a2a-9090-99d6fd140ea9">IBDA_ConditionalAccessEx::CheckEntitlementToken</a>



<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


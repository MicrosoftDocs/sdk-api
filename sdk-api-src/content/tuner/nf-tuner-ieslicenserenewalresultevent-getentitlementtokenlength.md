---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetEntitlementTokenLength
title: IESLicenseRenewalResultEvent::GetEntitlementTokenLength
author: windows-sdk-content
description: Gets the length of the entitlement token in a protected-content license from a LicenseRenewalResult event.
old-location: mstv\ieslicenserenewalresultevent_getentitlementtokenlength.htm
old-project: mstv
ms.assetid: e1c8f12c-c2f1-48c1-90fc-051ac87863d5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEntitlementTokenLength, GetEntitlementTokenLength method [DirectShow], GetEntitlementTokenLength method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetEntitlementTokenLength method, IESLicenseRenewalResultEvent.GetEntitlementTokenLength, IESLicenseRenewalResultEvent::GetEntitlementTokenLength, mstv.ieslicenserenewalresultevent_getentitlementtokenlength, tuner/IESLicenseRenewalResultEvent::GetEntitlementTokenLength
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESLicenseRenewalResultEvent.GetEntitlementTokenLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESLicenseRenewalResultEvent::GetEntitlementTokenLength


## -description


Gets the length of the entitlement token in a protected-content license from a <b>LicenseRenewalResult</b> event.


## -parameters




### -param pdwLength [out, retval]

Receives the length of the entitlement token, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


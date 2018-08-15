---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetEntitlementToken
title: IESLicenseRenewalResultEvent::GetEntitlementToken
author: windows-sdk-content
description: Gets the entitlement token in a protected-content license from a LicenseRenewalResult event. Clients can call the GetEntitlementTokenLength method to get the number of bytes to read from this buffer.
old-location: mstv\ieslicenserenewalresultevent_getentitlementtoken.htm
old-project: mstv
ms.assetid: 6178a884-df87-4fcb-a069-3791726d4335
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetEntitlementToken, GetEntitlementToken method [DirectShow], GetEntitlementToken method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetEntitlementToken method, IESLicenseRenewalResultEvent.GetEntitlementToken, IESLicenseRenewalResultEvent::GetEntitlementToken, mstv.ieslicenserenewalresultevent_getentitlementtoken, tuner/IESLicenseRenewalResultEvent::GetEntitlementToken
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
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
 - IESLicenseRenewalResultEvent.GetEntitlementToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESLicenseRenewalResultEvent::GetEntitlementToken


## -description


 Gets the entitlement token in a protected-content license from a <b>LicenseRenewalResult</b> event. Clients can call the <a href="https://msdn.microsoft.com/e1c8f12c-c2f1-48c1-90fc-051ac87863d5">GetEntitlementTokenLength</a> method to get the number of bytes to read from this buffer.


## -parameters




### -param pbData






#### - BYTE [out, retval]

Pointer to a buffer that receives the entitlement token. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e1c8f12c-c2f1-48c1-90fc-051ac87863d5">GetEntitlementTokenLength</a>



<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


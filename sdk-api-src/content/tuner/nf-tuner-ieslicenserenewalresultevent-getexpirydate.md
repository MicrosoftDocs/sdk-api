---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetExpiryDate
title: IESLicenseRenewalResultEvent::GetExpiryDate
author: windows-sdk-content
description: Gets the expiry date of a renewed protected-content license from a LicenseRenewalResult event.
old-location: mstv\ieslicenserenewalresultevent_getexpirydate.htm
tech.root: MSTV
ms.assetid: b237eeb3-d04f-432a-8c7a-538882b5ad02
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetExpiryDate, GetExpiryDate method [DirectShow], GetExpiryDate method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetExpiryDate method, IESLicenseRenewalResultEvent.GetExpiryDate, IESLicenseRenewalResultEvent::GetExpiryDate, mstv.ieslicenserenewalresultevent_getexpirydate, tuner/IESLicenseRenewalResultEvent::GetExpiryDate
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
 - IESLicenseRenewalResultEvent.GetExpiryDate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESLicenseRenewalResultEvent::GetExpiryDate


## -description


 Gets the expiry date of a renewed protected-content license from a <b>LicenseRenewalResult</b> event.


## -parameters




### -param pqwExpiryDate [out, retval]

Receives the expiry date in number of seconds since epoch.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


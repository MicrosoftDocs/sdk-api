---
UID: NF:tuner.IESLicenseRenewalResultEvent.IsRenewalSuccessful
title: IESLicenseRenewalResultEvent::IsRenewalSuccessful
author: windows-driver-content
description: Gets a flag from a LicenseRenewalResult event that indicates whether the renewal was successful. In the event of failure, a client can call the GetRenewalResultCode or GetRenewalHResult method to get information about the reason for the failure.
old-location: mstv\ieslicenserenewalresultevent_isrenewalsuccessful.htm
old-project: mstv
ms.assetid: 0c57e4e4-ee93-4e86-b1f8-eed5dd5aa931
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IESLicenseRenewalResultEvent interface [DirectShow],IsRenewalSuccessful method, IESLicenseRenewalResultEvent.IsRenewalSuccessful, IESLicenseRenewalResultEvent::IsRenewalSuccessful, IsRenewalSuccessful, IsRenewalSuccessful method [DirectShow], IsRenewalSuccessful method [DirectShow],IESLicenseRenewalResultEvent interface, mstv.ieslicenserenewalresultevent_isrenewalsuccessful, tuner/IESLicenseRenewalResultEvent::IsRenewalSuccessful
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
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESLicenseRenewalResultEvent.IsRenewalSuccessful
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESLicenseRenewalResultEvent::IsRenewalSuccessful


## -description


 Gets a flag from a  <b>LicenseRenewalResult</b> event that indicates whether the renewal was successful. In the event of failure, a client can call the  <a href="https://msdn.microsoft.com/99b46541-8c94-4456-aae9-d266fc52a6a9">GetRenewalResultCode</a> or <a href="https://msdn.microsoft.com/ed823c23-ae7d-4e2d-8546-92f04bd3b212">GetRenewalHResult</a> method to get information about the reason for the failure.


## -parameters




### -param pfRenewalSuccessful [out, retval]

Receives the renewal success flag: 1 indicates success; 0 indicates failure.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ed823c23-ae7d-4e2d-8546-92f04bd3b212">GetRenewalHResult</a>



<a href="https://msdn.microsoft.com/99b46541-8c94-4456-aae9-d266fc52a6a9">GetRenewalResultCode</a>



<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetCASFailureCode
title: IESLicenseRenewalResultEvent::GetCASFailureCode
author: windows-driver-content
description: Gets a code from a LicenseRenewalResult event that indicates the reason for the failure in the conditional access system (CAS).
old-location: mstv\ieslicenserenewalresultevent_getcasfailurecode.htm
old-project: mstv
ms.assetid: d3569a5e-6bde-4daf-bf52-094f56b0891c
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetCASFailureCode, GetCASFailureCode method [DirectShow], GetCASFailureCode method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetCASFailureCode method, IESLicenseRenewalResultEvent.GetCASFailureCode, IESLicenseRenewalResultEvent::GetCASFailureCode, mstv.ieslicenserenewalresultevent_getcasfailurecode, tuner/IESLicenseRenewalResultEvent::GetCASFailureCode
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
-	IESLicenseRenewalResultEvent.GetCASFailureCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESLicenseRenewalResultEvent::GetCASFailureCode


## -description


 Gets a code from a  <b>LicenseRenewalResult</b> event that indicates the reason for the failure in the conditional access system (CAS).


## -parameters




### -param pdwCASFailureCode [out, retval]

Receives the CAS failure code. This code is defined by the CAS that is used.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


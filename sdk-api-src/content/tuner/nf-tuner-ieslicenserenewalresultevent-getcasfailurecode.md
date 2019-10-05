---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetCASFailureCode
title: IESLicenseRenewalResultEvent::GetCASFailureCode (tuner.h)
author: windows-sdk-content
description: Gets a code from a LicenseRenewalResult event that indicates the reason for the failure in the conditional access system (CAS).
old-location: mstv\ieslicenserenewalresultevent_getcasfailurecode.htm
tech.root: mstv
ms.assetid: d3569a5e-6bde-4daf-bf52-094f56b0891c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCASFailureCode, GetCASFailureCode method [DirectShow], GetCASFailureCode method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetCASFailureCode method, IESLicenseRenewalResultEvent.GetCASFailureCode, IESLicenseRenewalResultEvent::GetCASFailureCode, mstv.ieslicenserenewalresultevent_getcasfailurecode, tuner/IESLicenseRenewalResultEvent::GetCASFailureCode
ms.topic: method
f1_keywords: 
 - "tuner/IESLicenseRenewalResultEvent.GetCASFailureCode"
dev_langs:
 - c++
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
 - IESLicenseRenewalResultEvent.GetCASFailureCode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>
 

 


---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetRenewalHResult
title: IESLicenseRenewalResultEvent::GetRenewalHResult
author: windows-driver-content
description: Gets the final HRESULT value from a LicenseRenewalResult event that is returned by a call to a COM interface method during the renewal process.
old-location: mstv\ieslicenserenewalresultevent_getrenewalhresult.htm
old-project: mstv
ms.assetid: ed823c23-ae7d-4e2d-8546-92f04bd3b212
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetRenewalHResult, GetRenewalHResult method [DirectShow], GetRenewalHResult method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetRenewalHResult method, IESLicenseRenewalResultEvent.GetRenewalHResult, IESLicenseRenewalResultEvent::GetRenewalHResult, mstv.ieslicenserenewalresultevent_getrenewalhresult, tuner/IESLicenseRenewalResultEvent::GetRenewalHResult
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
-	IESLicenseRenewalResultEvent.GetRenewalHResult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESLicenseRenewalResultEvent::GetRenewalHResult


## -description



      Gets the final <b>HRESULT</b> value from a  <b>LicenseRenewalResult</b> event that is returned by a call to a COM interface method during the renewal process. 


## -parameters




### -param phr [out, retval]

Receives the <b>HRESULT</b> value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


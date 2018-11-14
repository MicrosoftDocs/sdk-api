---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetCallersId
title: IESLicenseRenewalResultEvent::GetCallersId
author: windows-sdk-content
description: Gets a unique identifier from a LicenseRenewalResult event that identifies the caller.
old-location: mstv\ieslicenserenewalresultevent_getcallersid.htm
tech.root: MSTV
ms.assetid: c1dfbd63-c165-4872-b992-3f536be9cad1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCallersId, GetCallersId method [DirectShow], GetCallersId method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetCallersId method, IESLicenseRenewalResultEvent.GetCallersId, IESLicenseRenewalResultEvent::GetCallersId, mstv.ieslicenserenewalresultevent_getcallersid, tuner/IESLicenseRenewalResultEvent::GetCallersId
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
 - IESLicenseRenewalResultEvent.GetCallersId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tuner.h
: 
- IESLicenseRenewalResultEvent.GetCallersId
: 
---

# IESLicenseRenewalResultEvent::GetCallersId


## -description


 Gets a unique identifier from a <b>LicenseRenewalResult</b> event that identifies the caller. Each client that attempts to renew a license must specify this identifier to identify the client that is requesting the license renewal. When the renewal completes, this result is sent out and received by all the clients that are listening for this event. Clients can use this identifier value to match whether the result belongs to them or is intended for some other client.


## -parameters




### -param pdwCallersId [out, retval]

Receives the caller identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f9cbec4-7934-41fc-b387-3f45aa273a72">IESLicenseRenewalResultEvent</a>
 

 


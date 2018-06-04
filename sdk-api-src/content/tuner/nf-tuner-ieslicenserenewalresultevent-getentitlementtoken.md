---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


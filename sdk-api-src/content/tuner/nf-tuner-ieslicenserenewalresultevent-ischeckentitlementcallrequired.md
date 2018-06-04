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
 

 


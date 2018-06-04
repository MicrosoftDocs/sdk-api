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

# IWbemEventProviderSecurity::AccessCheck


## -description


The 
<b>AccessCheck</b> method is implemented by an event provider and called by Windows Management Instrumentation (WMI) when a consumer subscribes to an event specified in <i>wszQuery</i>.   A consumer that has access permission for an event can  subscribe to that event. A consumer that does not have access permission for an event cannot  subscribe to that event. For more information, see <a href="https://msdn.microsoft.com/075bdc65-4ea3-4f91-9823-1d2d0dc13423">Writing an Event Provider</a> and <a href="https://msdn.microsoft.com/86eaeb5c-c27e-4794-88e2-e0ffbb885290">Securing WMI Events</a>.

For a temporary consumer, WMI sets the <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">PSID</a> supplied in the <i>pSid</i> parameter to <b>NULL</b> and the call is made by impersonating the consumer.
For a permanent consumer, WMI sets the PSID with the security identifier (SID) of the user who created the subscription.


## -parameters




### -param wszQueryLanguage [in]

Language of the following query filter, which is "WQL".


### -param wszQuery [in]

Text of the event query filter, which is registered by a logical consumer.


### -param lSidLength [in]

Integer that contains the security identifier (SID) length, or 0 (zero) if the subscription builder token is available.


### -param pSid [in]

Pointer to the constant byte integer type that contains the SID, or <b>NULL</b> if the subscription builder's token is available.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained in an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/4b92923a-659d-4340-8843-eb42aea69d47">IWbemEventProvider </a>



<a href="https://msdn.microsoft.com/892a7a9d-f058-4c4d-870d-c0eb5773949f">IWbemEventProviderSecurity</a>



<a href="https://msdn.microsoft.com/8882fdcb-3768-41e3-82ab-3006d903f3a0">SELECT Statement for Event Queries</a>



<a href="https://msdn.microsoft.com/86eaeb5c-c27e-4794-88e2-e0ffbb885290">Securing WMI Events</a>
 

 


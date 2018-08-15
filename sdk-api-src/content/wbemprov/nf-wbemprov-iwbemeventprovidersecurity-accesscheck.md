---
UID: NF:wbemprov.IWbemEventProviderSecurity.AccessCheck
title: IWbemEventProviderSecurity::AccessCheck
author: windows-sdk-content
description: The AccessCheck method is implemented by an event provider and called by Windows Management Instrumentation (WMI) when a consumer subscribes to an event specified in wszQuery.
old-location: wmi\iwbemeventprovidersecurity_accesscheck.htm
old-project: WmiSdk
ms.assetid: 9c5cf37f-f43f-46c7-a5b4-1537aead158e
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: AccessCheck, AccessCheck method [Windows Management Instrumentation], AccessCheck method [Windows Management Instrumentation],IWbemEventProviderSecurity interface, IWbemEventProviderSecurity interface [Windows Management Instrumentation],AccessCheck method, IWbemEventProviderSecurity.AccessCheck, IWbemEventProviderSecurity::AccessCheck, _hmm_iwbemeventprovidersecurity_accesscheck, wbemprov/IWbemEventProviderSecurity::AccessCheck, wmi.iwbemeventprovidersecurity_accesscheck
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventProviderSecurity.AccessCheck
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 


---
UID: NF:wbemprov.IWbemEventProviderSecurity.AccessCheck
title: IWbemEventProviderSecurity::AccessCheck (wbemprov.h)
description: The AccessCheck method is implemented by an event provider and called by Windows Management Instrumentation (WMI) when a consumer subscribes to an event specified in wszQuery.
helpviewer_keywords: ["AccessCheck","AccessCheck method [Windows Management Instrumentation]","AccessCheck method [Windows Management Instrumentation]","IWbemEventProviderSecurity interface","IWbemEventProviderSecurity interface [Windows Management Instrumentation]","AccessCheck method","IWbemEventProviderSecurity.AccessCheck","IWbemEventProviderSecurity::AccessCheck","_hmm_iwbemeventprovidersecurity_accesscheck","wbemprov/IWbemEventProviderSecurity::AccessCheck","wmi.iwbemeventprovidersecurity_accesscheck"]
old-location: wmi\iwbemeventprovidersecurity_accesscheck.htm
tech.root: wmi
ms.assetid: 9c5cf37f-f43f-46c7-a5b4-1537aead158e
ms.date: 12/05/2018
ms.keywords: AccessCheck, AccessCheck method [Windows Management Instrumentation], AccessCheck method [Windows Management Instrumentation],IWbemEventProviderSecurity interface, IWbemEventProviderSecurity interface [Windows Management Instrumentation],AccessCheck method, IWbemEventProviderSecurity.AccessCheck, IWbemEventProviderSecurity::AccessCheck, _hmm_iwbemeventprovidersecurity_accesscheck, wbemprov/IWbemEventProviderSecurity::AccessCheck, wmi.iwbemeventprovidersecurity_accesscheck
req.header: wbemprov.h
req.include-header: Wbemidl.h
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
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemEventProviderSecurity::AccessCheck
 - wbemprov/IWbemEventProviderSecurity::AccessCheck
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventProviderSecurity.AccessCheck
---

# IWbemEventProviderSecurity::AccessCheck


## -description

The 
<b>AccessCheck</b> method is implemented by an event provider and called by Windows Management Instrumentation (WMI) when a consumer subscribes to an event specified in <i>wszQuery</i>.   A consumer that has access permission for an event can  subscribe to that event. A consumer that does not have access permission for an event cannot  subscribe to that event. For more information, see <a href="/windows/desktop/WmiSdk/writing-an-event-provider">Writing an Event Provider</a> and <a href="/windows/desktop/WmiSdk/securing-wmi-events">Securing WMI Events</a>.

For a temporary consumer, WMI sets the <a href="/windows/desktop/api/winnt/ns-winnt-sid">PSID</a> supplied in the <i>pSid</i> parameter to <b>NULL</b> and the call is made by impersonating the consumer.
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

<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemeventprovider">IWbemEventProvider </a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemeventprovidersecurity">IWbemEventProviderSecurity</a>



<a href="/windows/desktop/WmiSdk/select-statement-for-event-queries">SELECT Statement for Event Queries</a>



<a href="/windows/desktop/WmiSdk/securing-wmi-events">Securing WMI Events</a>
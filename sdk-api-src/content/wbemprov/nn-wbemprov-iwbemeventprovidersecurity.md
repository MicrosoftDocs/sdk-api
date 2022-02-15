---
UID: NN:wbemprov.IWbemEventProviderSecurity
title: IWbemEventProviderSecurity (wbemprov.h)
description: The IWbemEventProviderSecurity interface is optionally implemented by event providers who want to restrict consumer access to their event. For more information about when to use this interface, see Securing WMI Events.
helpviewer_keywords: ["IWbemEventProviderSecurity","IWbemEventProviderSecurity interface [Windows Management Instrumentation]","IWbemEventProviderSecurity interface [Windows Management Instrumentation]","described","_hmm_iwbemeventprovidersecurity","wbemprov/IWbemEventProviderSecurity","wmi.iwbemeventprovidersecurity"]
old-location: wmi\iwbemeventprovidersecurity.htm
tech.root: wmi
ms.assetid: 892a7a9d-f058-4c4d-870d-c0eb5773949f
ms.date: 12/05/2018
ms.keywords: IWbemEventProviderSecurity, IWbemEventProviderSecurity interface [Windows Management Instrumentation], IWbemEventProviderSecurity interface [Windows Management Instrumentation],described, _hmm_iwbemeventprovidersecurity, wbemprov/IWbemEventProviderSecurity, wmi.iwbemeventprovidersecurity
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
 - IWbemEventProviderSecurity
 - wbemprov/IWbemEventProviderSecurity
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
 - IWbemEventProviderSecurity
---

# IWbemEventProviderSecurity interface


## -description

The 
<b>IWbemEventProviderSecurity</b> interface is optionally implemented by event providers who want to restrict consumer access to their event. For more information about when to use this interface, see <a href="/windows/desktop/WmiSdk/securing-wmi-events">Securing WMI Events</a>.

## -inheritance

The <b>IWbemEventProviderSecurity</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemEventProviderSecurity</b> also has these types of members:

## -remarks

This method is automatically called by Windows Management whenever a new consumer attempts to subscribe to an event where the event provider has implemented 
<b>IWbemEventProviderSecurity</b>. If the consumer has access permission for the event the consumer is subscribed to the event; otherwise, the subscription is denied.

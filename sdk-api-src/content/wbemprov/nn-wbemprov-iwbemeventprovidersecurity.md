---
UID: NN:wbemprov.IWbemEventProviderSecurity
title: IWbemEventProviderSecurity
author: windows-sdk-content
description: The IWbemEventProviderSecurity interface is optionally implemented by event providers who want to restrict consumer access to their event. For more information about when to use this interface, see Securing WMI Events.
old-location: wmi\iwbemeventprovidersecurity.htm
tech.root: WmiSdk
ms.assetid: 892a7a9d-f058-4c4d-870d-c0eb5773949f
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemEventProviderSecurity, IWbemEventProviderSecurity interface [Windows Management Instrumentation], IWbemEventProviderSecurity interface [Windows Management Instrumentation],described, _hmm_iwbemeventprovidersecurity, wbemprov/IWbemEventProviderSecurity, wmi.iwbemeventprovidersecurity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemEventProviderSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemEventProviderSecurity interface


## -description


The 
<b>IWbemEventProviderSecurity</b> interface is optionally implemented by event providers who want to restrict consumer access to their event. For more information about when to use this interface, see <a href="https://msdn.microsoft.com/86eaeb5c-c27e-4794-88e2-e0ffbb885290">Securing WMI Events</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemEventProviderSecurity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemEventProviderSecurity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemEventProviderSecurity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c5cf37f-f43f-46c7-a5b4-1537aead158e">AccessCheck</a>
</td>
<td align="left" width="63%">
Checks a consumer's access permission when the consumer attempts to subscribe to an event.

</td>
</tr>
</table> 


## -remarks



This method is automatically called by Windows Management whenever a new consumer attempts to subscribe to an event where the event provider has implemented 
<b>IWbemEventProviderSecurity</b>. If the consumer has access permission for the event the consumer is subscribed to the event; otherwise, the subscription is denied.




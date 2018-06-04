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

# IWbemEventProvider::ProvideEvents


## -description


Windows Management calls the 
<b>IWbemEventProvider::ProvideEvents</b> method to signal an event provider to begin delivery of its events.


## -parameters




### -param pSink [in]

Pointer to the object sink to which the provider will deliver its events. In an event provider implementation, you should use the 
<a href="https://msdn.microsoft.com/96756b27-cbcf-47ce-a8c8-88795a81edde">IWbemObjectSink::Indicate</a> method to send events through <i>pSink</i>. This is in contrast to other providers that may use the 
<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">SetStatus</a> method: The 
<b>ProvideEvents</b> method should use only 
<b>Indicate</b> to update a sink.


### -param lFlags [in]

Reserved. This parameter must be 0.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




## -remarks



Windows Management calls this method to activate the provider. Windows Management gives an 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> pointer to the event provider. The provider must call the <b>AddRef</b> method using this pointer to increment the reference count, and then return from the call.

Typically, the provider will create an independent thread, and deliver the events as they occur to the provided sink interface.

The provider is not permitted to block this call for more than a few seconds, but it must return as quickly as possible to Windows Management.




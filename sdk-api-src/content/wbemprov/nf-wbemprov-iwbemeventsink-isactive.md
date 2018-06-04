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

# IWbemEventSink::IsActive


## -description


The 
<b>IWbemEventSink::IsActive</b> method is used by the provider to determine if there is interest in the events that the sink is filtering. In the case of a restricted sink, these events are defined by the queries passed to 
<a href="https://msdn.microsoft.com/f72ab8f7-e4de-4f64-80db-6981b0bd13d3">GetRestrictedSink</a>. In the case where it is not a restricted sink, these events are defined by the queries in the event provider's registration. In the latter, the sink is always active.


## -parameters






## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




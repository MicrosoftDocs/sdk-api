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

# IWbemEventSink::GetRestrictedSink


## -description


The 
<b>IWbemEventSink::GetRestrictedSink</b> method retrieves a restricted event sink. A restricted event sink is one which filters a subset of the events defined in the event provider's registration.


## -parameters




### -param lNumQueries [in]

Number of queries in array.


### -param awszQueries [in]

Array of event queries.


### -param pCallback [in]

Pointer to callback for event provider.


### -param ppSink [out]

Pointer to created 
<a href="https://msdn.microsoft.com/dd076dd0-ed39-47a2-86fb-a595baf3f464">IWbemEventSink</a> object.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




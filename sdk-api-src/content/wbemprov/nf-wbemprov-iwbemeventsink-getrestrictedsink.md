---
UID: NF:wbemprov.IWbemEventSink.GetRestrictedSink
title: IWbemEventSink::GetRestrictedSink
author: windows-sdk-content
description: The IWbemEventSink::GetRestrictedSink method retrieves a restricted event sink. A restricted event sink is one which filters a subset of the events defined in the event provider's registration.
old-location: wmi\iwbemeventsink_getrestrictedsink.htm
old-project: WmiSdk
ms.assetid: f72ab8f7-e4de-4f64-80db-6981b0bd13d3
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetRestrictedSink, GetRestrictedSink method [Windows Management Instrumentation], GetRestrictedSink method [Windows Management Instrumentation],IWbemEventSink interface, IWbemEventSink interface [Windows Management Instrumentation],GetRestrictedSink method, IWbemEventSink.GetRestrictedSink, IWbemEventSink::GetRestrictedSink, _hmm_iwbemeventsink_getrestrictedsink, wbemprov/IWbemEventSink::GetRestrictedSink, wmi.iwbemeventsink_getrestrictedsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IWbemEventSink.GetRestrictedSink
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
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




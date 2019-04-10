---
UID: NF:wbemprov.IWbemDecoupledBasicEventProvider.GetSink
title: IWbemDecoupledBasicEventProvider::GetSink (wbemprov.h)
author: windows-sdk-content
description: The IWbemDecoupledBasicEventProvider::GetSink method retrieves an IWbemObjectSink object for event forwarding to WMI. This method provides for fully concurrent access.
old-location: wmi\iwbemdecoupledbasiceventprovider_getsink.htm
tech.root: WmiSdk
ms.assetid: 2b33e441-4bc4-47ed-b09b-7af859127b06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSink, GetSink method [Windows Management Instrumentation], GetSink method [Windows Management Instrumentation],IWbemDecoupledBasicEventProvider interface, GetSink method [Windows Management Instrumentation],WbemDecoupledBasicEventProvider object, IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation],GetSink method, IWbemDecoupledBasicEventProvider.GetSink, IWbemDecoupledBasicEventProvider::GetSink, WbemDecoupledBasicEventProvider object [Windows Management Instrumentation],GetSink method, _hmm_iwbemdecoupledbasiceventprovider_getsink, wbemprov/IWbemDecoupledBasicEventProvider::GetSink, wmi.iwbemdecoupledbasiceventprovider_getsink
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
req.idl: Wbemprov.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmidcprv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmidcprv.dll
api_name:
 - IWbemDecoupledBasicEventProvider.GetSink
 - WbemDecoupledBasicEventProvider.GetSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemDecoupledBasicEventProvider::GetSink


## -description


The 
<b>IWbemDecoupledBasicEventProvider::GetSink</b> method retrieves an 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> object for event forwarding to WMI. This method provides for fully concurrent access.


## -parameters




### -param a_Flags [in]

Reserved for future use.


### -param a_Context [in]

Reserved for future use.


### -param a_Sink [out]

Pointer to an 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> instance used to forward events to WMI.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




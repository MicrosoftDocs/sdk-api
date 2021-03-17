---
UID: NF:wbemprov.IWbemDecoupledBasicEventProvider.GetSink
title: IWbemDecoupledBasicEventProvider::GetSink (wbemprov.h)
description: The IWbemDecoupledBasicEventProvider::GetSink method retrieves an IWbemObjectSink object for event forwarding to WMI. This method provides for fully concurrent access.
helpviewer_keywords: ["GetSink","GetSink method [Windows Management Instrumentation]","GetSink method [Windows Management Instrumentation]","IWbemDecoupledBasicEventProvider interface","GetSink method [Windows Management Instrumentation]","WbemDecoupledBasicEventProvider object","IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation]","GetSink method","IWbemDecoupledBasicEventProvider.GetSink","IWbemDecoupledBasicEventProvider::GetSink","WbemDecoupledBasicEventProvider object [Windows Management Instrumentation]","GetSink method","_hmm_iwbemdecoupledbasiceventprovider_getsink","wbemprov/IWbemDecoupledBasicEventProvider::GetSink","wmi.iwbemdecoupledbasiceventprovider_getsink"]
old-location: wmi\iwbemdecoupledbasiceventprovider_getsink.htm
tech.root: wmi
ms.assetid: 2b33e441-4bc4-47ed-b09b-7af859127b06
ms.date: 12/05/2018
ms.keywords: GetSink, GetSink method [Windows Management Instrumentation], GetSink method [Windows Management Instrumentation],IWbemDecoupledBasicEventProvider interface, GetSink method [Windows Management Instrumentation],WbemDecoupledBasicEventProvider object, IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation],GetSink method, IWbemDecoupledBasicEventProvider.GetSink, IWbemDecoupledBasicEventProvider::GetSink, WbemDecoupledBasicEventProvider object [Windows Management Instrumentation],GetSink method, _hmm_iwbemdecoupledbasiceventprovider_getsink, wbemprov/IWbemDecoupledBasicEventProvider::GetSink, wmi.iwbemdecoupledbasiceventprovider_getsink
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemDecoupledBasicEventProvider::GetSink
 - wbemprov/IWbemDecoupledBasicEventProvider::GetSink
dev_langs:
 - c++
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
---

# IWbemDecoupledBasicEventProvider::GetSink


## -description

The 
<b>IWbemDecoupledBasicEventProvider::GetSink</b> method retrieves an 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> object for event forwarding to WMI. This method provides for fully concurrent access.

## -parameters

### -param a_Flags [in]

Reserved for future use.

### -param a_Context [in]

Reserved for future use.

### -param a_Sink [out]

Pointer to an 
<a href="/windows/desktop/WmiSdk/iwbemobjectsink">IWbemObjectSink</a> instance used to forward events to WMI.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.
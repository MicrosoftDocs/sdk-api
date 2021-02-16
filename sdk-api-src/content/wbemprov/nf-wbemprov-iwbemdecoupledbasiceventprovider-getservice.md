---
UID: NF:wbemprov.IWbemDecoupledBasicEventProvider.GetService
title: IWbemDecoupledBasicEventProvider::GetService (wbemprov.h)
description: The IWbemDecoupledBasicEventProvider::GetService method retrieves an IWbemService object to be used to call back into WMI. This method provides for fully concurrent access.
helpviewer_keywords: ["GetService","GetService method [Windows Management Instrumentation]","GetService method [Windows Management Instrumentation]","IWbemDecoupledBasicEventProvider interface","GetService method [Windows Management Instrumentation]","WbemDecoupledBasicEventProvider object","IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation]","GetService method","IWbemDecoupledBasicEventProvider.GetService","IWbemDecoupledBasicEventProvider::GetService","WbemDecoupledBasicEventProvider object [Windows Management Instrumentation]","GetService method","_hmm_iwbemdecoupledbasiceventprovider_getservice","wbemprov/IWbemDecoupledBasicEventProvider::GetService","wmi.iwbemdecoupledbasiceventprovider_getservice"]
old-location: wmi\iwbemdecoupledbasiceventprovider_getservice.htm
tech.root: wmi
ms.assetid: d9ce6d1b-4e4a-4d36-8957-85471fff3c69
ms.date: 12/05/2018
ms.keywords: GetService, GetService method [Windows Management Instrumentation], GetService method [Windows Management Instrumentation],IWbemDecoupledBasicEventProvider interface, GetService method [Windows Management Instrumentation],WbemDecoupledBasicEventProvider object, IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation],GetService method, IWbemDecoupledBasicEventProvider.GetService, IWbemDecoupledBasicEventProvider::GetService, WbemDecoupledBasicEventProvider object [Windows Management Instrumentation],GetService method, _hmm_iwbemdecoupledbasiceventprovider_getservice, wbemprov/IWbemDecoupledBasicEventProvider::GetService, wmi.iwbemdecoupledbasiceventprovider_getservice
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
 - IWbemDecoupledBasicEventProvider::GetService
 - wbemprov/IWbemDecoupledBasicEventProvider::GetService
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
 - IWbemDecoupledBasicEventProvider.GetService
 - WbemDecoupledBasicEventProvider.GetService
---

# IWbemDecoupledBasicEventProvider::GetService


## -description

The 
<b>IWbemDecoupledBasicEventProvider::GetService</b> method retrieves an <b>IWbemService</b> object to be used to call back into WMI. This method provides for fully concurrent access.

## -parameters

### -param a_Flags [in]

Reserved for future use.

### -param a_Context [in]

Reserved for future use.

### -param a_Service [out]

Pointer to an <b>IWbemService</b> object that can be used to retrieve information from WMI.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.


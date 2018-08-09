---
UID: NF:wbemprov.IWbemDecoupledBasicEventProvider.GetService
title: IWbemDecoupledBasicEventProvider::GetService
author: windows-sdk-content
description: The IWbemDecoupledBasicEventProvider::GetService method retrieves an IWbemService object to be used to call back into WMI. This method provides for fully concurrent access.
old-location: wmi\iwbemdecoupledbasiceventprovider_getservice.htm
old-project: WmiSdk
ms.assetid: d9ce6d1b-4e4a-4d36-8957-85471fff3c69
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: GetService, GetService method [Windows Management Instrumentation], GetService method [Windows Management Instrumentation],IWbemDecoupledBasicEventProvider interface, GetService method [Windows Management Instrumentation],WbemDecoupledBasicEventProvider object, IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation],GetService method, IWbemDecoupledBasicEventProvider.GetService, IWbemDecoupledBasicEventProvider::GetService, WbemDecoupledBasicEventProvider object [Windows Management Instrumentation],GetService method, _hmm_iwbemdecoupledbasiceventprovider_getservice, wbemprov/IWbemDecoupledBasicEventProvider::GetService, wmi.iwbemdecoupledbasiceventprovider_getservice
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
req.idl: Wbemprov.idl
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
 - Wmidcprv.dll
api_name:
 - IWbemDecoupledBasicEventProvider.GetService
 - WbemDecoupledBasicEventProvider.GetService
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmidcprv.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemDecoupledBasicEventProvider::GetService


## -description


The 
<b>IWbemDecoupledBasicEventProvider::GetService</b> method retrieves an <b>IWbemService</b> object to be used to call back into WMI. This method provides for fully concurrent access.


## -parameters




### -param a_Flags




### -param a_Context




### -param a_Service






#### - lFlags [in]

Reserved for future use.


#### - pContext [in]

Reserved for future use.


#### - pService [out]

Pointer to an <b>IWbemService</b> object that can be used to retrieve information from WMI.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




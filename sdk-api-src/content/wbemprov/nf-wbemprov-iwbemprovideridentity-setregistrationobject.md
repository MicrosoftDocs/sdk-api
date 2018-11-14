---
UID: NF:wbemprov.IWbemProviderIdentity.SetRegistrationObject
title: IWbemProviderIdentity::SetRegistrationObject
author: windows-sdk-content
description: The IWbemProviderIdentity::SetRegistrationObject method is called by the Windows Management service prior to initializing an event provider (if the provider implements IWbemProviderIdentity).
old-location: wmi\iwbemprovideridentity_setregistrationobject.htm
tech.root: WmiSdk
ms.assetid: e600d562-6a93-422c-88f2-d44196191843
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IWbemProviderIdentity interface [Windows Management Instrumentation],SetRegistrationObject method, IWbemProviderIdentity.SetRegistrationObject, IWbemProviderIdentity::SetRegistrationObject, SetRegistrationObject, SetRegistrationObject method [Windows Management Instrumentation], SetRegistrationObject method [Windows Management Instrumentation],IWbemProviderIdentity interface, _hmm_iwbemprovideridentity_setregistrationobject, wbemprov/IWbemProviderIdentity::SetRegistrationObject, wmi.iwbemprovideridentity_setregistrationobject
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWbemProviderIdentity.SetRegistrationObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wbemprov.h
: 
- IWbemProviderIdentity.SetRegistrationObject
: 
---

# IWbemProviderIdentity::SetRegistrationObject


## -description


The 
<b>IWbemProviderIdentity::SetRegistrationObject</b> method is called by the Windows Management service prior to initializing an event provider (if the provider implements 
<a href="https://msdn.microsoft.com/872daa72-c6ff-4c6d-a870-c32e3688eb13">IWbemProviderIdentity</a>). The method is used to pass to the provider the 
<a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a> instance by which the provider is being initialized. This method is only used if you have more than one provider sharing the same <b>CLSID</b>.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param pProvReg [in]

Instance of 
<a href="https://msdn.microsoft.com/41e0d938-00c6-4f4c-8027-8b8512398dee">__Win32Provider</a> that announces the provider's name and <b>CLSID</b>.


## -returns



This method returns an <b>HRESULT</b> with one of the following values.




## -remarks



Any <b>HRESULT</b> return code other than <b>WBEM_S_NO_ERROR</b> indicates a provider failure.




## -see-also




<a href="https://msdn.microsoft.com/872daa72-c6ff-4c6d-a870-c32e3688eb13">IWbemProviderIdentity</a>
 

 


---
UID: NF:wbemprov.IWbemProviderIdentity.SetRegistrationObject
title: IWbemProviderIdentity::SetRegistrationObject (wbemprov.h)
description: The IWbemProviderIdentity::SetRegistrationObject method is called by the Windows Management service prior to initializing an event provider (if the provider implements IWbemProviderIdentity).
helpviewer_keywords: ["IWbemProviderIdentity interface [Windows Management Instrumentation]","SetRegistrationObject method","IWbemProviderIdentity.SetRegistrationObject","IWbemProviderIdentity::SetRegistrationObject","SetRegistrationObject","SetRegistrationObject method [Windows Management Instrumentation]","SetRegistrationObject method [Windows Management Instrumentation]","IWbemProviderIdentity interface","_hmm_iwbemprovideridentity_setregistrationobject","wbemprov/IWbemProviderIdentity::SetRegistrationObject","wmi.iwbemprovideridentity_setregistrationobject"]
old-location: wmi\iwbemprovideridentity_setregistrationobject.htm
tech.root: wmi
ms.assetid: e600d562-6a93-422c-88f2-d44196191843
ms.date: 12/05/2018
ms.keywords: IWbemProviderIdentity interface [Windows Management Instrumentation],SetRegistrationObject method, IWbemProviderIdentity.SetRegistrationObject, IWbemProviderIdentity::SetRegistrationObject, SetRegistrationObject, SetRegistrationObject method [Windows Management Instrumentation], SetRegistrationObject method [Windows Management Instrumentation],IWbemProviderIdentity interface, _hmm_iwbemprovideridentity_setregistrationobject, wbemprov/IWbemProviderIdentity::SetRegistrationObject, wmi.iwbemprovideridentity_setregistrationobject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemProviderIdentity::SetRegistrationObject
 - wbemprov/IWbemProviderIdentity::SetRegistrationObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemProviderIdentity.SetRegistrationObject
---

# IWbemProviderIdentity::SetRegistrationObject


## -description

The 
<b>IWbemProviderIdentity::SetRegistrationObject</b> method is called by the Windows Management service prior to initializing an event provider (if the provider implements 
<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemprovideridentity">IWbemProviderIdentity</a>). The method is used to pass to the provider the 
<a href="/windows/desktop/WmiSdk/--win32provider">__Win32Provider</a> instance by which the provider is being initialized. This method is only used if you have more than one provider sharing the same <b>CLSID</b>.

## -parameters

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param pProvReg [in]

Instance of 
<a href="/windows/desktop/WmiSdk/--win32provider">__Win32Provider</a> that announces the provider's name and <b>CLSID</b>.

## -returns

This method returns an <b>HRESULT</b> with one of the following values.

## -remarks

Any <b>HRESULT</b> return code other than <b>WBEM_S_NO_ERROR</b> indicates a provider failure.

## -see-also

<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemprovideridentity">IWbemProviderIdentity</a>
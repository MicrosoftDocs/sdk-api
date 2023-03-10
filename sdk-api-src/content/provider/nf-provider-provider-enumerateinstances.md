---
UID: NF:provider.Provider.EnumerateInstances
title: Provider::EnumerateInstances (provider.h)
description: The EnumerateInstances method is called by WMI to retrieve all instances of a framework provider's class.
helpviewer_keywords: ["?EnumerateInstances@Provider@@MAEJPAVMethodContext@@J@Z","EnumerateInstances","EnumerateInstances method [Windows Management Instrumentation]","EnumerateInstances method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","EnumerateInstances method","Provider.EnumerateInstances","Provider::EnumerateInstances","_hmm_provider_enumerateinstances","provider/Provider::EnumerateInstances","wmi.provider_enumerateinstances"]
old-location: wmi\provider_enumerateinstances.htm
tech.root: wmi
ms.assetid: 9566acb0-d7bf-4d3d-b7da-5cfbce150a2c
ms.date: 12/05/2018
ms.keywords: ?EnumerateInstances@Provider@@MAEJPAVMethodContext@@J@Z, EnumerateInstances, EnumerateInstances method [Windows Management Instrumentation], EnumerateInstances method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],EnumerateInstances method, Provider.EnumerateInstances, Provider::EnumerateInstances, _hmm_provider_enumerateinstances, provider/Provider::EnumerateInstances, wmi.provider_enumerateinstances
req.header: provider.h
req.include-header: FwCommon.h
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
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Provider::EnumerateInstances
 - provider/Provider::EnumerateInstances
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.EnumerateInstances
 - ?EnumerateInstances@Provider@@MAEJPAVMethodContext@@J@Z
---

# Provider::EnumerateInstances


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>EnumerateInstances</b> method is called by WMI to retrieve all instances of a framework provider's class.

## -parameters

### -param pMethodContext

Pointer to the context object for this call. This value contains any <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> properties specified by the client. Also, this pointer must be used as a parameter to any calls back into WMI.

### -param lFlags

Bitmask of flags with information about the <b>EnumerateInstances</b> operation. This is the value specified by the client in the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a> method.

The following flags are handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_DEEP</b></li>
<li><b>WBEM_FLAG_SHALLOW</b></li>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
<li><b>WBEM_FLAG_FORWARD_ONLY</b></li>
<li><b>WBEM_FLAG_BIDIRECTIONAL</b></li>
<li><b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b></li>
</ul>

## -returns

The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a> method lists the most common return values, but you can choose to return any COM return code.

## -remarks

It is not an error for <b>EnumerateInstances</b> to return zero instances by instantiating zero <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> instances and setting the return value to <b>WBEM_S_NO_ERROR</b>.

WMI often calls <b>EnumerateInstances</b> when a client application calls <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">IWbemServices::CreateInstanceEnum</a>, although WMI may call <b>EnumerateInstances</b> in other situations as well. The following is a common way to override <b>EnumerateInstances</b>:

<ol>
<li>Create an empty instance of your class using <a href="/windows/desktop/api/provider/nf-provider-provider-createnewinstance">Provider::CreateNewInstance</a>.</li>
<li>Populate the properties of the empty instance using the Set methods of the <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class, such as <a href="/windows/desktop/api/instance/nf-instance-cinstance-setbyte">CInstance::SetByte</a> or <a href="/windows/desktop/api/instance/nf-instance-cinstance-setstringarray">CInstance::SetStringArray</a>.</li>
<li>Send the instance back to the client using <a href="/windows/desktop/api/instance/nf-instance-cinstance-commit">CInstance::Commit</a>.</li>
</ol>
If you are building a method-only provider and do not have any instances, or if enumerating instances of your class would return too many instances, you may decide to support queries that retrieve only specific instances.
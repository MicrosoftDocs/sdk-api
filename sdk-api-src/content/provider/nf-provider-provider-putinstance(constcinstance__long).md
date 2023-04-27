---
UID: NF:provider.Provider.PutInstance(constCInstance&,long)
title: Provider::PutInstance(const CInstance &,long) (provider.h)
description: The PutInstance method updates an instance. (overload 2/2)
helpviewer_keywords: ["Provider interface [Windows Management Instrumentation]","PutInstance method","Provider.PutInstance","Provider.PutInstance(const CInstance &","long)","Provider::PutInstance","Provider::PutInstance(const CInstance &","long)","PutInstance","PutInstance method [Windows Management Instrumentation]","PutInstance method [Windows Management Instrumentation]","Provider interface","_hmm_provider_putinstance","provider/Provider::PutInstance","wmi.provider_putinstance"]
old-location: wmi\provider_putinstance.htm
tech.root: wmi
ms.assetid: c9921a00-b966-47d0-a2f3-982812ab249c
ms.date: 12/05/2018
ms.keywords: Provider interface [Windows Management Instrumentation],PutInstance method, Provider.PutInstance, Provider.PutInstance(const CInstance &,long), Provider::PutInstance, Provider::PutInstance(const CInstance &,long), PutInstance, PutInstance method [Windows Management Instrumentation], PutInstance method [Windows Management Instrumentation],Provider interface, _hmm_provider_putinstance, provider/Provider::PutInstance, wmi.provider_putinstance
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
 - Provider::PutInstance
 - provider/Provider::PutInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.PutInstance
---

# Provider::PutInstance(const CInstance &,long)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class is part of the WMI 
    Provider Framework which is now considered in final state, and no further development, enhancements, or updates 
    will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>PutInstance</b> method updates an instance.

## -parameters

### -param newInstance [ref]

Instance that is updated.

### -param lFlags

Bitmask of flags with information about the update operation. This is the value specified by the client in the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a> method.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>
Valid <i>lFlags</i> values are:

<ul>
<li><b>WBEM_FLAG_CREATE_ONLY</b></li>
<li><b>WBEM_FLAG_CREATE_OR_UPDATE</b></li>
<li><b>WBEM_FLAG_UPDATE_ONLY</b></li>
</ul>

## -returns

The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a> method lists the most common return values, although you can choose to return any COM return code.

## -remarks

WMI invokes <b>PutInstance</b> when a client calls <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a> against your class. You must implement <b>PutInstance</b> if your framework provider updates instances. The following list describes a common implementation of <b>PutInstance</b>:

<ol>
<li>
Examine the key properties passed in by the client with the Get methods for <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>, such as <a href="/windows/desktop/api/instance/nf-instance-cinstance-getchstring">CInstance::GetCHString</a>.

Your implementation should determine if your provider supports the changes requested by the client.

</li>
<li>Create or update the appropriate managed object, as necessary.</li>
<li>
Return the appropriate return value.

If your provider does not support the changes requested by the client, you should return an appropriate error code. For a complete listing of valid error codes, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>.

</li>
</ol>

---
UID: NF:provider.Provider.GetObject(ParsedObjectPath,MethodContext,long)
title: Provider::GetObject(ParsedObjectPath,MethodContext,long) (provider.h)
description: The GetObject method is called by WMI to retrieve an instance of a class.
helpviewer_keywords: ["?GetObject@Provider@@MAEJPAVCInstance@@JAAVCFrameworkQuery@@@Z","?GetObject@Provider@@MEAAJPEAVCInstance@@JAEAVCFrameworkQuery@@@Z","GetObject","GetObject method [Windows Management Instrumentation]","GetObject method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","GetObject method","Provider.GetObject","Provider.GetObject(ParsedObjectPath","MethodContext","long)","Provider::GetObject","Provider::GetObject(ParsedObjectPath","MethodContext","long)","_hmm_provider_getobject","provider/Provider::GetObject","wmi.provider_getobject"]
old-location: wmi\provider_getobject.htm
tech.root: wmi
ms.assetid: c8e2633a-cbea-422c-9598-1b1b1104bbc2
ms.date: 12/05/2018
ms.keywords: ?GetObject@Provider@@MAEJPAVCInstance@@JAAVCFrameworkQuery@@@Z, ?GetObject@Provider@@MEAAJPEAVCInstance@@JAEAVCFrameworkQuery@@@Z, GetObject, GetObject method [Windows Management Instrumentation], GetObject method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],GetObject method, Provider.GetObject, Provider.GetObject(ParsedObjectPath,MethodContext,long), Provider::GetObject, Provider::GetObject(ParsedObjectPath,MethodContext,long), _hmm_provider_getobject, provider/Provider::GetObject, wmi.provider_getobject
f1_keywords:
- provider/Provider.GetObject
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
api_name:
- Provider.GetObject
- ?GetObject@Provider@@MAEJPAVCInstance@@JAAVCFrameworkQuery@@@Z
- ?GetObject@Provider@@MEAAJPEAVCInstance@@JAEAVCFrameworkQuery@@@Z
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Provider::GetObject(ParsedObjectPath,MethodContext,long)


## -description


<p class="CCE_Message">[The <a href="https://docs.microsoft.com/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>GetObject</b> method is called by WMI to retrieve an instance of a class.


## -parameters




#### - pParsedObjectPath

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> object to be filled in by the framework provider.


#### - pContext

Bitmask of flags with information about the <b>GetObject</b> operation. This is the value specified by the client in the <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> method.

The following flags are handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b></li>
<li><b>WBEM_FLAG_RETURN_WBEM_COMPLETE</b></li>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>

### -param lFlags [ref]

Query object that indicates the set of properties to be populated, as requested by a call to <b>Provider::GetObject</b>.

A provider can realize a significant performance gain by filling in only these requested property values. The provider determines which properties are requested by using <a href="https://docs.microsoft.com/windows/desktop/api/frquery/nf-frquery-cframeworkquery-ispropertyrequired">CFrameworkQuery::IsPropertyRequired</a>. Otherwise, the provider must fill in all property values.


## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a> method lists the common return values, although you can choose to implement any COM return value.




## -remarks



WMI often invokes <b>GetObject</b> in response to a client call to <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a>. The WMI version of <b>Provider::GetObject</b> provides an instance with only the key properties populated. In contrast, an implemented framework provider must fill in all other properties. The following describes a common override of <b>GetObject</b>:

<ol>
<li>Determine which instance WMI requested by reading the key properties with a <b>Get</b> method from <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a>, such as <a href="https://docs.microsoft.com/windows/desktop/api/instance/nf-instance-cinstance-getchstring">CInstance::GetCHString</a>.</li>
<li>Populate the rest of the properties of the instance using the many Set methods of the <a href="https://docs.microsoft.com/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class, such as <a href="https://docs.microsoft.com/windows/desktop/api/instance/nf-instance-cinstance-setbyte">CInstance::SetByte</a> or <a href="https://docs.microsoft.com/windows/desktop/api/instance/nf-instance-cinstance-setstringarray">CInstance::SetStringArray</a>.</li>
</ol>



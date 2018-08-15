---
UID: NF:provider.Provider.GetObject
title: Provider::GetObject
author: windows-sdk-content
description: The GetObject method is called by WMI to retrieve an instance of a class.
old-location: wmi\provider_getobject.htm
old-project: WmiSdk
ms.assetid: c8e2633a-cbea-422c-9598-1b1b1104bbc2
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "?GetObject@Provider@@MAEJPAVCInstance@@JAAVCFrameworkQuery@@@Z, ?GetObject@Provider@@MEAAJPEAVCInstance@@JAEAVCFrameworkQuery@@@Z, GetObject, GetObject method [Windows Management Instrumentation], GetObject method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],GetObject method, Provider.GetObject, Provider::GetObject, _hmm_provider_getobject, provider/Provider::GetObject, wmi.provider_getobject"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: provider.h
req.include-header: FwCommon.h
req.redist: 
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
req.typenames: PROPVAR_COMPARE_UNIT
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
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: ADAM
---

# Provider::GetObject


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetObject</b> method is called by WMI to retrieve an instance of a class.


## -parameters




#### - pInstance

Pointer to a <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> object to be filled in by the framework provider.


### -param lFlags

Bitmask of flags with information about the <b>GetObject</b> operation. This is the value specified by the client in the <a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a> method.

The following flags are handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b></li>
<li><b>WBEM_FLAG_RETURN_WBEM_COMPLETE</b></li>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>

#### - Query [ref]

Query object that indicates the set of properties to be populated, as requested by a call to <b>Provider::GetObject</b>.

A provider can realize a significant performance gain by filling in only these requested property values. The provider determines which properties are requested by using <a href="https://msdn.microsoft.com/36f5a261-435c-494d-aae5-a420eee030f2">CFrameworkQuery::IsPropertyRequired</a>. Otherwise, the provider must fill in all property values.


## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a> method lists the common return values, although you can choose to implement any COM return value.




## -remarks



WMI often invokes <b>GetObject</b> in response to a client call to <a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>. The WMI version of <b>Provider::GetObject</b> provides an instance with only the key properties populated. In contrast, an implemented framework provider must fill in all other properties. The following describes a common override of <b>GetObject</b>:

<ol>
<li>Determine which instance WMI requested by reading the key properties with a <b>Get</b> method from <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>, such as <a href="https://msdn.microsoft.com/d9295ba1-19da-41a2-86d1-ec80e18e895b">CInstance::GetCHString</a>.</li>
<li>Populate the rest of the properties of the instance using the many Set methods of the <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class, such as <a href="https://msdn.microsoft.com/d6ecbada-4eb6-40ad-9e59-ba77fd3b883a">CInstance::SetByte</a> or <a href="https://msdn.microsoft.com/dcd1e108-4914-43ea-aa41-d38d38e8954a">CInstance::SetStringArray</a>.</li>
</ol>



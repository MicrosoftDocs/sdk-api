---
UID: NF:provider.Provider.ExecMethod(const CInstance &,const BSTR,CInstance,CInstance,long)
title: Provider::ExecMethod(const CInstance &,const BSTR,CInstance,CInstance,long)
author: windows-sdk-content
description: The ExecMethod method is called by WMI to invoke a method on a class or instance.
old-location: wmi\provider_execmethod.htm
tech.root: WmiSdk
ms.assetid: 590f59ad-ea93-42f0-8b0d-c05a49272b1b
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ExecMethod, ExecMethod method [Windows Management Instrumentation], ExecMethod method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],ExecMethod method, Provider.ExecMethod, Provider.ExecMethod(const CInstance &,const BSTR,CInstance,CInstance,long), Provider::ExecMethod, Provider::ExecMethod(const CInstance &,const BSTR,CInstance,CInstance,long), _hmm_provider_execmethod, provider/Provider::ExecMethod, wmi.provider_execmethod
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - Provider.ExecMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Provider::ExecMethod(const CInstance &,const BSTR,CInstance,CInstance,long)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>ExecMethod</b> method is called by WMI to invoke a method on a class or instance.


## -parameters




### -param cInstance

TBD


### -param bstrMethodName

Name of the method that is invoked.


### -param pInParams

Pointer to the method input parameters.


### -param pOutParams

Pointer to the method output parameters.


### -param lFlags

Bitmask of flags with information about the execute method operation. This is the value specified by the client in the <a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a> method. Few clients use the <i>lFlags</i> parameters. You can safely ignore <i>lFlags</i> in most provider implementations.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>

#### - Instance [ref]

Key properties of the instance in question if the client called an instance method. If the client called a static method, <i>Instance</i> contains a class object.


## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a> method lists the most common return values, although you can choose to return any COM return code.

Return values for methods may be one of two types:

<ul>
<li><b>HRESULT</b> is used to indicate WMI type errors: <b>WBEM_E_OUT_OF_MEMORY</b>, <b>WBEM_E_NOT_FOUND</b>, and so on.</li>
<li>The return value from the method (such as <b>uint32</b>) returns the result from the method.</li>
</ul>



## -remarks



WMI calls <b>ExecMethod</b> when a client calls <a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a> against your class. Therefore, you must implement <b>ExecMethod</b> if your provider supports one or more methods. The following list describes a common implementation of <b>ExecMethod</b>:

<ol>
<li>Determine which method the client called by examining the <i>bstrMethodName</i> parameter.</li>
<li>
Retrieve the input parameters from the <i>pInParams</i> parameter, using the <b>Get</b> methods from the <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class, such as <a href="https://msdn.microsoft.com/d9295ba1-19da-41a2-86d1-ec80e18e895b">CInstance::GetCHString</a>.

A method may have input parameters, output parameters, both input and output parameters, or no input or output parameters.

</li>
<li>
Set the output parameters in the <i>pOutParams</i> parameter, using the Set methods of the <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class, such as <a href="https://msdn.microsoft.com/d6ecbada-4eb6-40ad-9e59-ba77fd3b883a">CInstance::SetByte</a> or <a href="https://msdn.microsoft.com/dcd1e108-4914-43ea-aa41-d38d38e8954a">CInstance::SetStringArray</a>.

In addition to declaring the [out] properties as specified in the return declaration, you must also declare the return value for the method, as defined in the <b>ReturnValue</b> property. You do not have to declare a return value if if the return value is <b>void</b>.

</li>
</ol>
For more information, see <a href="https://msdn.microsoft.com/9acba1aa-bcca-416a-863c-704d2e72df07">IWbemServices::ExecMethod</a>.




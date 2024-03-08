---
UID: NF:provider.Provider.ExecMethod(ParsedObjectPath,BSTR,long,CInstance,CInstance,MethodContext)
title: Provider::ExecMethod(ParsedObjectPath,BSTR,long,CInstance,CInstance,MethodContext) (provider.h)
description: The ExecMethod method is called by WMI to invoke a method on a class or instance. (overload 2/2)
helpviewer_keywords: ["ExecMethod","ExecMethod method [Windows Management Instrumentation]","ExecMethod method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","ExecMethod method","Provider.ExecMethod","Provider.ExecMethod(ParsedObjectPath","BSTR","long","CInstance","CInstance","MethodContext)","Provider::ExecMethod","Provider::ExecMethod(ParsedObjectPath","BSTR","long","CInstance","CInstance","MethodContext)","_hmm_provider_execmethod","provider/Provider::ExecMethod","wmi.provider_execmethod"]
old-location: wmi\provider_execmethod.htm
tech.root: wmi
ms.assetid: 590f59ad-ea93-42f0-8b0d-c05a49272b1b
ms.date: 12/05/2018
ms.keywords: ExecMethod, ExecMethod method [Windows Management Instrumentation], ExecMethod method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],ExecMethod method, Provider.ExecMethod, Provider.ExecMethod(ParsedObjectPath,BSTR,long,CInstance,CInstance,MethodContext), Provider::ExecMethod, Provider::ExecMethod(ParsedObjectPath,BSTR,long,CInstance,CInstance,MethodContext), _hmm_provider_execmethod, provider/Provider::ExecMethod, wmi.provider_execmethod
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
 - Provider::ExecMethod
 - provider/Provider::ExecMethod
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
 - Provider.ExecMethod
---

# Provider::ExecMethod(ParsedObjectPath,BSTR,long,CInstance,CInstance,MethodContext)


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ExecMethod</b> method is called by WMI to invoke a method on a class or instance.

## -parameters

### -param pParsedObjectPath

TBD

### -param bstrMethodName

Name of the method that is invoked.

### -param lFlags

Bitmask of flags with information about the execute method operation. This is the value specified by the client in the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a> method. Few clients use the <i>lFlags</i> parameters. You can safely ignore <i>lFlags</i> in most provider implementations.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>

### -param pInParams

Pointer to the method input parameters.

### -param pOutParams

Pointer to the method output parameters.

### -param pContext

TBD




#### - cInstance [ref]

Key properties of the instance in question if the client called an instance method. If the client called a static method, <i>Instance</i> contains a class object.

## -returns

The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a> method lists the most common return values, although you can choose to return any COM return code.

Return values for methods may be one of two types:

<ul>
<li><b>HRESULT</b> is used to indicate WMI type errors: <b>WBEM_E_OUT_OF_MEMORY</b>, <b>WBEM_E_NOT_FOUND</b>, and so on.</li>
<li>The return value from the method (such as <b>uint32</b>) returns the result from the method.</li>
</ul>

## -remarks

WMI calls <b>ExecMethod</b> when a client calls <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a> against your class. Therefore, you must implement <b>ExecMethod</b> if your provider supports one or more methods. The following list describes a common implementation of <b>ExecMethod</b>:

<ol>
<li>Determine which method the client called by examining the <i>bstrMethodName</i> parameter.</li>
<li>
Retrieve the input parameters from the <i>pInParams</i> parameter, using the <b>Get</b> methods from the <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class, such as <a href="/windows/desktop/api/instance/nf-instance-cinstance-getchstring">CInstance::GetCHString</a>.

A method may have input parameters, output parameters, both input and output parameters, or no input or output parameters.

</li>
<li>
Set the output parameters in the <i>pOutParams</i> parameter, using the Set methods of the <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class, such as <a href="/windows/desktop/api/instance/nf-instance-cinstance-setbyte">CInstance::SetByte</a> or <a href="/windows/desktop/api/instance/nf-instance-cinstance-setstringarray">CInstance::SetStringArray</a>.

In addition to declaring the [out] properties as specified in the return declaration, you must also declare the return value for the method, as defined in the <b>ReturnValue</b> property. You do not have to declare a return value if the return value is <b>void</b>.

</li>
</ol>
For more information, see <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod">IWbemServices::ExecMethod</a>.

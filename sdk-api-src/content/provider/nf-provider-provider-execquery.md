---
UID: NF:provider.Provider.ExecQuery
title: Provider::ExecQuery (provider.h)
description: The ExecQuery method is called by WMI to process a WMI Query Language (WQL) query.
helpviewer_keywords: ["ExecQuery","ExecQuery method [Windows Management Instrumentation]","ExecQuery method [Windows Management Instrumentation]","Provider interface","Provider interface [Windows Management Instrumentation]","ExecQuery method","Provider.ExecQuery","Provider::ExecQuery","_hmm_provider_execquery","provider/Provider::ExecQuery","wmi.provider_execquery"]
old-location: wmi\provider_execquery.htm
tech.root: wmi
ms.assetid: 94d5c8ee-2d61-42af-9a22-cc0df423b245
ms.date: 12/05/2018
ms.keywords: ExecQuery, ExecQuery method [Windows Management Instrumentation], ExecQuery method [Windows Management Instrumentation],Provider interface, Provider interface [Windows Management Instrumentation],ExecQuery method, Provider.ExecQuery, Provider::ExecQuery, _hmm_provider_execquery, provider/Provider::ExecQuery, wmi.provider_execquery
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
 - Provider::ExecQuery
 - provider/Provider::ExecQuery
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
 - Provider.ExecQuery
---

# Provider::ExecQuery


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ExecQuery</b> method is called by WMI to process a WMI Query Language (WQL) query.

## -parameters

### -param pMethodContext

Pointer to the context object for this call. This value contains any <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> properties specified by the client. Also, this pointer must be used as a parameter to any calls back into WMI.

### -param cQuery [ref]

Pointer to a query that has already been parsed by the provider framework.

### -param lFlags

Bitmask of flags with information about the execute query operation. This is the value specified by the client in the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a> method.

The following flags are handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_ENSURE_LOCATABLE</b></li>
<li><b>WBEM_FLAG_FORWARD_ONLY</b></li>
<li><b>WBEM_FLAG_BIDIRECTIONAL</b></li>
<li><b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b></li>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
<li><b>WBEM_FLAG_PROTOTYPE</b></li>
</ul>

## -returns

The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a> method lists the common return values, although you can choose to return any COM return code.

## -remarks

WMI often calls <b>ExecQuery</b> in response to a client call to <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a>, where the client passes in either a list of selected properties or a WHERE clause. WMI can also call <b>ExecQuery</b> if the client query contains an "ASSOCIATORS OF" or "REFERENCES OF" statement describing your class. If your implementation of <b>ExecQuery</b> returns <b>WBEM_E_NOT_SUPPORTED</b>, the client relies on WMI to handle the query.

WMI handles a query by calling your implementation of <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum">CreateInstanceEnum</a> to provide all the instances. WMI then filters the resulting instances before returning the instances to the client. Therefore, any implementation of <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">ExecQuery</a> you create must be more efficient than <b>CreateInstanceEnum</b>.

The following describes a common implementation of <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">ExecQuery</a>:

<ol>
<li>Create an empty instance of your class using <a href="/windows/desktop/api/provider/nf-provider-provider-createnewinstance">Provider::CreateNewInstance</a>.</li>
<li>
Determine the subset of instances that you should create.

You can use methods such as <a href="/windows/desktop/api/frquery/nf-frquery-cframeworkquery-ispropertyrequired">IsPropertyRequired</a> to see what properties are required, and <a href="/windows/desktop/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_)">GetValuesForProp</a> to see what instances WMI requires. Other methods that deal with requested properties include <a href="/windows/desktop/api/frquery/nf-frquery-cframeworkquery-getrequiredproperties">CFrameworkQuery::GetRequiredProperties</a>,  <a href="/windows/desktop/api/frquery/nf-frquery-cframeworkquery-allpropertiesarerequired">CFrameworkQuery::AllPropertiesAreRequired</a>, and <a href="/windows/desktop/api/frquery/nf-frquery-cframeworkquery-keysonly">CFrameworkQuery::KeysOnly</a>.

</li>
<li>Populate the properties of the empty instance using the Set methods of the <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> class, such as <a href="/windows/desktop/api/instance/nf-instance-cinstance-setbyte">CInstance::SetByte</a> or <a href="/windows/desktop/api/instance/nf-instance-cinstance-setstringarray">CInstance::SetStringArray</a>.</li>
<li>Send the instance back to the client using <a href="/windows/desktop/api/instance/nf-instance-cinstance-commit">CInstance::Commit</a>.</li>
<li>
Return the appropriate return values.

The default <b>ExecQuery</b> framework provider implementation returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>. If you implement <b>ExecQuery</b>, you should use the common return values listed in <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery">IWbemServices::ExecQuery</a>. If necessary, however, you can return any COM return code.

</li>
</ol>
WMI does not send "ASSOCIATORS OF" or "REFERENCES OF" queries through to framework providers. Instead, WMI uses the schema to determine which classes are related to the class in question, and generates an appropriate WQL query to retrieve the results. Therefore, you do not need to code any additional support of "ASSOCIATORS OF" and "REFERENCES OF" queries.

However, you should keep the following in mind when writing your framework provider:

<ul>
<li>Make sure you support standard queries in your association class, especially queries where the reference properties are used in a WHERE clause. For more information, see <a href="/windows/desktop/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_)">CFrameworkQuery::GetValuesForProp</a>.</li>
<li>
In your association class support, when you check to see if the endpoints exist, ensure you use the <a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancekeysbypath">CWbemProviderGlue::GetInstanceKeysByPath</a> or <a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancepropertiesbypath">CWbemProviderGlue::GetInstancePropertiesByPath</a> methods.

These methods allow the endpoints to skip populating  resource-intensive or unneeded properties.

</li>
<li>Make sure any association endpoint classes support per-property <b>Get</b> methods. For more information, see <a href="/windows/desktop/WmiSdk/supporting-partial-instance-operations">Supporting Partial-Instance Operations</a>. For more information about the query parameter, see <a href="/windows/desktop/api/frquery/nl-frquery-cframeworkquery">CFrameworkQuery</a>.</li>
</ul>
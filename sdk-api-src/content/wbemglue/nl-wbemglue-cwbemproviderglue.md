---
UID: NL:wbemglue.CWbemProviderGlue
title: CWbemProviderGlue (wbemglue.h)
description: CWbemProviderGlue ties the Component Object Model (COM) interfaces of the Windows Management Instrumentation (WMI) API to the classes derived from the Provider class, and supplies methods for providers to use to query each other.
helpviewer_keywords: ["CWbemProviderGlue","CWbemProviderGlue class [Windows Management Instrumentation]","CWbemProviderGlue class [Windows Management Instrumentation]","described","_hmm_cwbemproviderglue","wbemglue/CWbemProviderGlue","wmi.cwbemproviderglue"]
old-location: wmi\cwbemproviderglue.htm
tech.root: wmi
ms.assetid: 493027c2-e54d-4fad-9e33-98d1ceab8860
ms.date: 12/05/2018
ms.keywords: CWbemProviderGlue, CWbemProviderGlue class [Windows Management Instrumentation], CWbemProviderGlue class [Windows Management Instrumentation],described, _hmm_cwbemproviderglue, wbemglue/CWbemProviderGlue, wmi.cwbemproviderglue
req.header: wbemglue.h
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
 - CWbemProviderGlue
 - wbemglue/CWbemProviderGlue
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
 - CWbemProviderGlue
---

# CWbemProviderGlue class


## -description

<p class="CCE_Message">[The <b>CWbemProviderGlue</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

<b>CWbemProviderGlue</b>  ties the Component Object Model (COM) interfaces of the Windows Management Instrumentation (WMI) API to the classes derived from the <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class, and supplies methods for providers to use to query each other. It is not expected that provider writers ever derive from this class, or create instances of this class. Typically, the provider writer  uses the static methods listed here to retrieve information from WMI. The <b>CWbemProviderGlue</b> is a COM interface, and it relies on COM security for  interprocess communication. For more information, see <a href="/windows/desktop/WmiSdk/setting-the-security-levels-on-a-wmi-connection">Setting the Security Levels on a WMI Connection</a> and <a href="/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies">Setting the Security on IWbemServices and Other Proxies</a>.

<b>CWbemProviderGlue</b> has these types of members:
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)">FrameworkLoginDLL</a>
</td>
<td align="left" width="63%">
Called when the DLL_PROCESS_ATTACH value is sent to <a href="/windows/desktop/Dlls/dllmain">DllMain</a> to determine whether the provider server can be loaded.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)">FrameworkLogoffDLL</a>
</td>
<td align="left" width="63%">
Called by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow">DllCanUnloadNow</a> to determine whether the provider server is not in use and can be unloaded.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr)">GetAllDerivedInstances</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances derived from a particular base class.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallderivedinstancesasynch">GetAllDerivedInstancesAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider and derived from a particular base class. Returns one instance at a time.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances">GetAllInstances</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstancesasynch">GetAllInstancesAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider. Returns one instance at a time.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr)">GetEmptyInstance</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a single instance from a particular provider.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext)">GetInstanceByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancekeysbypath">GetInstanceKeysByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path, with only the key properties populated.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancepropertiesbypath">GetInstancePropertiesByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path, with only the specified properties populated.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr)">GetInstancesByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances that match a particular query.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getinstancesbyqueryasynch">GetInstancesByQueryAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider that match a particular query. Returns one instance at a time.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext)">GetNamespaceConnection</a>
</td>
<td align="left" width="63%">
Retrieves a namespace connection.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr)">IsDerivedFrom</a>
</td>
<td align="left" width="63%">
Determines whether one class is derived from another.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-setstatusobject">SetStatusObject</a>
</td>
<td align="left" width="63%">
Sets the parameters of a status object which is used to supply more information when an error occurs.

</td>
</tr>
</table>

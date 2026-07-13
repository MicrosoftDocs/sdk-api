---
UID: NL:provider.Provider
title: Provider (provider.h)
description: The Provider class is the base class for the class or classes that the framework provider supports.
helpviewer_keywords: ["??1Provider@@UAE@XZ","??1Provider@@UEAA@XZ","Provider","Provider class [Windows Management Instrumentation]","Provider class [Windows Management Instrumentation]","described","_hmm_provider","provider/Provider","wmi.provider"]
old-location: wmi\provider.htm
tech.root: wmi
ms.assetid: d8a7c433-7e6a-45cc-914f-a15a3688c7aa
ms.date: 12/05/2018
ms.keywords: ??1Provider@@UAE@XZ, ??1Provider@@UEAA@XZ, Provider, Provider class [Windows Management Instrumentation], Provider class [Windows Management Instrumentation],described, _hmm_provider, provider/Provider, wmi.provider
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
 - Provider
 - provider/Provider
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
 - sqlmgmprovider.dll
api_name:
 - Provider
 - ??1Provider@@UAE@XZ
 - ??1Provider@@UEAA@XZ
---

# Provider class


## -description

<p class="CCE_Message">[The <b>Provider</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>Provider</b> class is the base class for the class or classes that the framework provider supports. The <b>Provider</b> class encapsulates implementations of the methods of <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> and includes several helper functions. A framework provider overrides one of the methods of the <b>Provider</b> class for each feature that it supports. For example, a provider that supports query processing overrides the <a href="/windows/desktop/api/provider/nf-provider-provider-execquery">Provider::ExecQuery</a> method.

An instance of the <b>Provider</b> class is created for each WMI class that has a framework provider.

<b>Provider</b> has these types of members:
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-commit">Commit</a>
</td>
<td align="left" width="63%">
Returns the current instance to WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-createnewinstance">CreateNewInstance</a>
</td>
<td align="left" width="63%">
Allocates a new <a href="/windows/desktop/api/instance/nl-instance-cinstance">CInstance</a> object and returns a pointer to it.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext)">DeleteInstance</a>
</td>
<td align="left" width="63%">
Deletes an instance. Called by WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-enumerateinstances">EnumerateInstances</a>
</td>
<td align="left" width="63%">
Retrieves all instances of a framework provider's class. Called by WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext)">ExecMethod</a>
</td>
<td align="left" width="63%">
Invokes a method on a class or instance. Called by WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-execquery">ExecQuery</a>
</td>
<td align="left" width="63%">
Processes a WMI Query Language (WQL) query. Called by WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-flush">Flush</a>
</td>
<td align="left" width="63%">
Called by the provider framework to delete all unnecessary memory in use by the provider.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-getlocalcomputername">GetLocalComputerName</a>
</td>
<td align="left" width="63%">
Returns a constant reference to the computer name in <a href="/windows/desktop/WmiSdk/chstring">CHString</a> format.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-getlocalinstancepath">GetLocalInstancePath</a>
</td>
<td align="left" width="63%">
Attempts to build a full object path to a specified instance.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an instance of a class. Called by WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-getprovidername">GetProviderName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the provider.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-makelocalpath">MakeLocalPath</a>
</td>
<td align="left" width="63%">
Builds a full instance path from a relative path.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-putinstance(constcinstance__long)">PutInstance</a>
</td>
<td align="left" width="63%">
Updates an instance. Called by WMI.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-setcreationclassname">SetCreationClassName</a>
</td>
<td align="left" width="63%">
Sets the <b>CreationClassName</b> string property of the given instance to the name of this provider.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-validatedeletionflags">ValidateDeletionFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for a delete operation.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-validateenumerationflags">ValidateEnumerationFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an enumeration.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-validateflags">ValidateFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-validategetobjflags">ValidateGetObjFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an instance retrieval operation.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-validatemethodflags">ValidateMethodFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an execute method operation.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-validateputinstanceflags">ValidatePutInstanceFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an instance update operation.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/provider/nf-provider-provider-validatequeryflags">ValidateQueryFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for a query operation.

</td>
</tr>
</table>

## -remarks

The destructor for this class is <b>Provider::~Provider</b>.

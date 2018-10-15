---
UID: NL:wbemglue.CWbemProviderGlue
title: CWbemProviderGlue
author: windows-sdk-content
description: CWbemProviderGlue ties the Component Object Model (COM) interfaces of the Windows Management Instrumentation (WMI) API to the classes derived from the Provider class, and supplies methods for providers to use to query each other.
old-location: wmi\cwbemproviderglue.htm
tech.root: WmiSdk
ms.assetid: 493027c2-e54d-4fad-9e33-98d1ceab8860
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CWbemProviderGlue, CWbemProviderGlue class [Windows Management Instrumentation], CWbemProviderGlue class [Windows Management Instrumentation],described, _hmm_cwbemproviderglue, wbemglue/CWbemProviderGlue, wmi.cwbemproviderglue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CWbemProviderGlue class


## -description


<p class="CCE_Message">[The <b>CWbemProviderGlue</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

<b>CWbemProviderGlue</b>  ties the Component Object Model (COM) interfaces of the Windows Management Instrumentation (WMI) API to the classes derived from the <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a> class, and supplies methods for providers to use to query each other. It is not expected that provider writers ever derive from this class, or create instances of this class. Typically, the provider writer  uses the static methods listed here to retrieve information from WMI. The <b>CWbemProviderGlue</b> is a COM interface, and it relies on COM security for  interprocess communication. For more information, see <a href="https://msdn.microsoft.com/dd453e0e-aa1f-4ef1-ab21-613630b2758c">Setting the Security Levels on a WMI Connection</a> and <a href="https://msdn.microsoft.com/83c04a96-3829-4c07-91a7-06e5b75b2c12">Setting the Security on IWbemServices and Other Proxies</a>.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CWbemProviderGlue</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>CWbemProviderGlue</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b701c70a-73f6-48b7-ab90-bbde1d29c9a2">FrameworkLoginDLL</a>
</td>
<td align="left" width="63%">
Called when the DLL_PROCESS_ATTACH value is sent to <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> to determine whether the provider server can be loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5157d823-d3a1-46d2-8ae8-07e904001a14">FrameworkLogoffDLL</a>
</td>
<td align="left" width="63%">
Called by <a href="_com_dllcanunloadnow">DllCanUnloadNow</a> to determine whether the provider server is not in use and can be unloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecdca316-12a0-46c3-97df-85a087533837">GetAllDerivedInstances</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances derived from a particular base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d58f8aca-2176-443e-b82a-87ee8bae8cf8">GetAllDerivedInstancesAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider and derived from a particular base class. Returns one instance at a time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/510d0711-ee82-4270-a7e3-f6bb214716a0">GetAllInstances</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58fe7757-c130-4859-9b60-d08bfb445eb1">GetAllInstancesAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider. Returns one instance at a time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2873b466-3782-4d63-a777-5b25e3fb7615">GetEmptyInstance</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a single instance from a particular provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/788b5f5f-b300-4c86-afbd-416b938f21c1">GetInstanceByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ae95850-59e9-4382-b88d-c51eb3077176">GetInstanceKeysByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path, with only the key properties populated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9232dc0-6df9-440d-bf7a-bf524acbe505">GetInstancePropertiesByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path, with only the specified properties populated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf086577-8964-4b6b-8863-78b53f73397e">GetInstancesByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances that match a particular query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51eccecb-5b92-4e06-89eb-552d97074629">GetInstancesByQueryAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider that match a particular query. Returns one instance at a time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abbc7099-400d-47a0-9673-3d102effa897">GetNamespaceConnection</a>
</td>
<td align="left" width="63%">
Retrieves a namespace connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8245511-d192-4489-b907-45de1d354c49">IsDerivedFrom</a>
</td>
<td align="left" width="63%">
Determines whether one class is derived from another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f094359-66ea-4604-85f8-1f6bc9a81cd1">SetStatusObject</a>
</td>
<td align="left" width="63%">
Sets the parameters of a status object which is used to supply more information when an error occurs.

</td>
</tr>
</table> 


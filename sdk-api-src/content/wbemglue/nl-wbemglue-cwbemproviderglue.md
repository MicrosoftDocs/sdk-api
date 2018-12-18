---
UID: NL:wbemglue.CWbemProviderGlue
title: CWbemProviderGlue
author: windows-sdk-content
description: CWbemProviderGlue ties the Component Object Model (COM) interfaces of the Windows Management Instrumentation (WMI) API to the classes derived from the Provider class, and supplies methods for providers to use to query each other.
old-location: wmi\cwbemproviderglue.htm
tech.root: WmiSdk
ms.assetid: 493027c2-e54d-4fad-9e33-98d1ceab8860
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CWbemProviderGlue, CWbemProviderGlue class [Windows Management Instrumentation], CWbemProviderGlue class [Windows Management Instrumentation],described, _hmm_cwbemproviderglue, wbemglue/CWbemProviderGlue, wmi.cwbemproviderglue
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

<b>CWbemProviderGlue</b>  ties the Component Object Model (COM) interfaces of the Windows Management Instrumentation (WMI) API to the classes derived from the <a href="https://msdn.microsoft.com/en-us/library/Aa392762(v=VS.85).aspx">Provider</a> class, and supplies methods for providers to use to query each other. It is not expected that provider writers ever derive from this class, or create instances of this class. Typically, the provider writer  uses the static methods listed here to retrieve information from WMI. The <b>CWbemProviderGlue</b> is a COM interface, and it relies on COM security for  interprocess communication. For more information, see <a href="https://msdn.microsoft.com/dd453e0e-aa1f-4ef1-ab21-613630b2758c">Setting the Security Levels on a WMI Connection</a> and <a href="https://msdn.microsoft.com/83c04a96-3829-4c07-91a7-06e5b75b2c12">Setting the Security on IWbemServices and Other Proxies</a>.

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
<a href="https://msdn.microsoft.com/en-us/library/Aa389782(v=VS.85).aspx">FrameworkLoginDLL</a>
</td>
<td align="left" width="63%">
Called when the DLL_PROCESS_ATTACH value is sent to <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> to determine whether the provider server can be loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389783(v=VS.85).aspx">FrameworkLogoffDLL</a>
</td>
<td align="left" width="63%">
Called by <a href="https://msdn.microsoft.com/en-us/library/ms690368(v=VS.85).aspx">DllCanUnloadNow</a> to determine whether the provider server is not in use and can be unloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389784(v=VS.85).aspx">GetAllDerivedInstances</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances derived from a particular base class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389785(v=VS.85).aspx">GetAllDerivedInstancesAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider and derived from a particular base class. Returns one instance at a time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389786(v=VS.85).aspx">GetAllInstances</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389787(v=VS.85).aspx">GetAllInstancesAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider. Returns one instance at a time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389788(v=VS.85).aspx">GetEmptyInstance</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a single instance from a particular provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389791(v=VS.85).aspx">GetInstanceByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389792(v=VS.85).aspx">GetInstanceKeysByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path, with only the key properties populated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389793(v=VS.85).aspx">GetInstancePropertiesByPath</a>
</td>
<td align="left" width="63%">
Retrieves the instance identified by a particular object path, with only the specified properties populated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389794(v=VS.85).aspx">GetInstancesByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances that match a particular query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389795(v=VS.85).aspx">GetInstancesByQueryAsynch</a>
</td>
<td align="left" width="63%">
Retrieves a list of instances supported by a particular provider that match a particular query. Returns one instance at a time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389796(v=VS.85).aspx">GetNamespaceConnection</a>
</td>
<td align="left" width="63%">
Retrieves a namespace connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389797(v=VS.85).aspx">IsDerivedFrom</a>
</td>
<td align="left" width="63%">
Determines whether one class is derived from another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa389798(v=VS.85).aspx">SetStatusObject</a>
</td>
<td align="left" width="63%">
Sets the parameters of a status object which is used to supply more information when an error occurs.

</td>
</tr>
</table> 


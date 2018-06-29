---
UID: NL:provider.Provider
title: Provider
author: windows-sdk-content
description: The Provider class is the base class for the class or classes that the framework provider supports.
old-location: wmi\provider.htm
old-project: WmiSdk
ms.assetid: d8a7c433-7e6a-45cc-914f-a15a3688c7aa
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "??1Provider@@UAE@XZ, ??1Provider@@UEAA@XZ, Provider, Provider class [Windows Management Instrumentation], Provider class [Windows Management Instrumentation],described, _hmm_provider, provider/Provider, wmi.provider"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
 - Provider
 - ??1Provider@@UAE@XZ
 - ??1Provider@@UEAA@XZ
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: ADAM
---

# Provider class


## -description


<p class="CCE_Message">[The <b>Provider</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Provider</b> class is the base class for the class or classes that the framework provider supports. The <b>Provider</b> class encapsulates implementations of the methods of <a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> and includes several helper functions. A framework provider overrides one of the methods of the <b>Provider</b> class for each feature that it supports. For example, a provider that supports query processing overrides the <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">Provider::ExecQuery</a> method.

An instance of the <b>Provider</b> class is created for each WMI class that has a framework provider.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Provider</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>Provider</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Returns the current instance to WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb520b55-9ef8-4f5a-935d-46c2bb01f5dd">CreateNewInstance</a>
</td>
<td align="left" width="63%">
Allocates a new <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> object and returns a pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/469d2481-95ea-4d17-b0ef-095ced9c8319">DeleteInstance</a>
</td>
<td align="left" width="63%">
Deletes an instance. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9566acb0-d7bf-4d3d-b7da-5cfbce150a2c">EnumerateInstances</a>
</td>
<td align="left" width="63%">
Retrieves all instances of a framework provider's class. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/590f59ad-ea93-42f0-8b0d-c05a49272b1b">ExecMethod</a>
</td>
<td align="left" width="63%">
Invokes a method on a class or instance. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">ExecQuery</a>
</td>
<td align="left" width="63%">
Processes a WMI Query Language (WQL) query. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Called by the provider framework to delete all unnecessary memory in use by the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20470353-417d-4067-8df1-c2ec6b330853">GetLocalComputerName</a>
</td>
<td align="left" width="63%">
Returns a constant reference to the computer name in <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c419205f-d07d-4887-8e36-ccde37c2351f">GetLocalInstancePath</a>
</td>
<td align="left" width="63%">
Attempts to build a full object path to a specified instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8e2633a-cbea-422c-9598-1b1b1104bbc2">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an instance of a class. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ea7558d-11bd-4f19-b4d3-a711eca632a8">GetProviderName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a2476c0-73c0-4a95-8973-e6da451116af">MakeLocalPath</a>
</td>
<td align="left" width="63%">
Builds a full instance path from a relative path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9921a00-b966-47d0-a2f3-982812ab249c">PutInstance</a>
</td>
<td align="left" width="63%">
Updates an instance. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a02e767-95b7-42cb-ab82-66e2d28342fc">SetCreationClassName</a>
</td>
<td align="left" width="63%">
Sets the <b>CreationClassName</b> string property of the given instance to the name of this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaaf49e3-e768-4494-ba0b-dc2c8c35be47">ValidateDeletionFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for a delete operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f5ae240-2314-40c1-a6c8-2c395d284568">ValidateEnumerationFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d6d1006-99b9-4646-a5c4-835940ce3ac0">ValidateFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5090c47b-062b-4359-b03b-0d05c225447d">ValidateGetObjFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an instance retrieval operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/febc48d8-8952-4e2f-80fc-40344908f8b2">ValidateMethodFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an execute method operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd7a480e-9569-45ed-a46d-218c1a9cf2db">ValidatePutInstanceFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an instance update operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b35e6f2f-7d40-4b9b-833d-63efafd06a20">ValidateQueryFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for a query operation.

</td>
</tr>
</table> 


## -remarks



The destructor for this class is <b>Provider::~Provider</b>.




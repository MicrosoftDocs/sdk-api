---
UID: NL:provider.Provider
title: Provider
author: windows-sdk-content
description: The Provider class is the base class for the class or classes that the framework provider supports.
old-location: wmi\provider.htm
tech.root: WmiSdk
ms.assetid: d8a7c433-7e6a-45cc-914f-a15a3688c7aa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "??1Provider@@UAE@XZ, ??1Provider@@UEAA@XZ, Provider, Provider class [Windows Management Instrumentation], Provider class [Windows Management Instrumentation],described, _hmm_provider, provider/Provider, wmi.provider"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Provider
 - ??1Provider@@UAE@XZ
 - ??1Provider@@UEAA@XZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Provider class


## -description


<p class="CCE_Message">[The <b>Provider</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Provider</b> class is the base class for the class or classes that the framework provider supports. The <b>Provider</b> class encapsulates implementations of the methods of <a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> and includes several helper functions. A framework provider overrides one of the methods of the <b>Provider</b> class for each feature that it supports. For example, a provider that supports query processing overrides the <a href="https://msdn.microsoft.com/en-us/library/Aa392770(v=VS.85).aspx">Provider::ExecQuery</a> method.

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
<a href="https://msdn.microsoft.com/en-us/library/Aa392763(v=VS.85).aspx">Commit</a>
</td>
<td align="left" width="63%">
Returns the current instance to WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392765(v=VS.85).aspx">CreateNewInstance</a>
</td>
<td align="left" width="63%">
Allocates a new <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> object and returns a pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392766(v=VS.85).aspx">DeleteInstance</a>
</td>
<td align="left" width="63%">
Deletes an instance. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392767(v=VS.85).aspx">EnumerateInstances</a>
</td>
<td align="left" width="63%">
Retrieves all instances of a framework provider's class. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392769(v=VS.85).aspx">ExecMethod</a>
</td>
<td align="left" width="63%">
Invokes a method on a class or instance. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392770(v=VS.85).aspx">ExecQuery</a>
</td>
<td align="left" width="63%">
Processes a WMI Query Language (WQL) query. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392771(v=VS.85).aspx">Flush</a>
</td>
<td align="left" width="63%">
Called by the provider framework to delete all unnecessary memory in use by the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392774(v=VS.85).aspx">GetLocalComputerName</a>
</td>
<td align="left" width="63%">
Returns a constant reference to the computer name in <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392775(v=VS.85).aspx">GetLocalInstancePath</a>
</td>
<td align="left" width="63%">
Attempts to build a full object path to a specified instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392779(v=VS.85).aspx">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an instance of a class. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392781(v=VS.85).aspx">GetProviderName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392881(v=VS.85).aspx">MakeLocalPath</a>
</td>
<td align="left" width="63%">
Builds a full instance path from a relative path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392883(v=VS.85).aspx">PutInstance</a>
</td>
<td align="left" width="63%">
Updates an instance. Called by WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392884(v=VS.85).aspx">SetCreationClassName</a>
</td>
<td align="left" width="63%">
Sets the <b>CreationClassName</b> string property of the given instance to the name of this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392885(v=VS.85).aspx">ValidateDeletionFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for a delete operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392886(v=VS.85).aspx">ValidateEnumerationFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392887(v=VS.85).aspx">ValidateFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392889(v=VS.85).aspx">ValidateGetObjFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an instance retrieval operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392890(v=VS.85).aspx">ValidateMethodFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an execute method operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392891(v=VS.85).aspx">ValidatePutInstanceFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for an instance update operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa392892(v=VS.85).aspx">ValidateQueryFlags</a>
</td>
<td align="left" width="63%">
Determines whether a set of flags is valid for a query operation.

</td>
</tr>
</table> 


## -remarks



The destructor for this class is <b>Provider::~Provider</b>.




---
UID: NN:wbemcli.IWbemQualifierSet
title: IWbemQualifierSet
author: windows-sdk-content
description: Acts as a container for the entire set of named qualifiers for a single property or entire object (a class or instance).
old-location: wmi\iwbemqualifierset.htm
tech.root: WmiSdk
ms.assetid: 8b36bd32-4931-4641-a019-cbaa3547edd0
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemQualifierSet, IWbemQualifierSet interface [Windows Management Instrumentation], IWbemQualifierSet interface [Windows Management Instrumentation],described, _hmm_iwbemqualifierset, wbemcli/IWbemQualifierSet, wmi.iwbemqualifierset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
api_name:
 - IWbemQualifierSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemQualifierSet interface


## -description


The 
<b>IWbemQualifierSet</b> interface acts as a container for the entire set of named qualifiers for a single property or entire object (a class or instance). The contents of the container depend on how the pointer was obtained. If the pointer was obtained from 
<a href="https://msdn.microsoft.com/da86b723-8126-44b9-95ec-120d88390ef3">IWbemClassObject::GetQualifierSet</a>, the object consists of the set of qualifiers for an entire object. If the pointer was obtained from 
<a href="https://msdn.microsoft.com/4bfca42e-7688-42e1-afa3-24b7eaaad9fe">IWbemClassObject::GetPropertyQualifierSet</a>, then the object represents the qualifiers for a particular property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemQualifierSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemQualifierSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemQualifierSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57fa60d1-54d2-412d-b39b-c35dfd709d0c">BeginEnumeration</a>
</td>
<td align="left" width="63%">
Resets prior to an enumeration of all qualifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77e61fd1-a835-4ed7-8880-9eab65611ebc">Delete</a>
</td>
<td align="left" width="63%">
Deletes the specified named qualifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/317409e9-b098-404b-bc09-78b5b5ae7fc7">EndEnumeration</a>
</td>
<td align="left" width="63%">
Ends an enumeration of qualifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4663cd1-0dc9-4021-918e-d5eda1648429">Get</a>
</td>
<td align="left" width="63%">
Reads a particular named qualifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1e7f6b2-a204-4e00-87eb-686bf8696082">GetNames</a>
</td>
<td align="left" width="63%">
Gets the names of qualifiers subject to certain filters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76afa293-1bd9-442b-bc9b-2247459bd49c">Next</a>
</td>
<td align="left" width="63%">
Gets the next qualifier during an enumeration of all qualifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad602440-dc19-45cf-bf10-a30f514e00bb">Put</a>
</td>
<td align="left" width="63%">
Writes a particular named qualifier.

</td>
</tr>
</table> 


## -remarks



It is strongly recommended that Windows Management dynamic providers never implement this interface because  WMI provides the implementation. For more information, see 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>.

Within WMI, this interface is always in-process. Put operations only affect the local copy of the object. Get operations retrieve values from the local copy. Updates are performed only when entire objects are read or written using methods on the 
<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>
 

 


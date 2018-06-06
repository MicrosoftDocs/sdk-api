---
UID: NL:methodco.MethodContext
title: MethodContext
author: windows-sdk-content
description: The MethodContext class is the pointer to a structure used in a provider to get or set IWbemClassObject information. WMI does not implement any functionality based on the pointer.
old-location: wmi\methodcontext.htm
old-project: WmiSdk
ms.assetid: aea20c9d-4042-426a-abdf-51ebddf017aa
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: MethodContext, MethodContext class [Windows Management Instrumentation], MethodContext class [Windows Management Instrumentation],described, methodco/MethodContext, wmi.methodcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: methodco.h
req.include-header: 
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
req.typenames: WIN32_MEMORY_REGION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MethodCo.h
api_name:
 - MethodContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MethodContext class


## -description


<p class="CCE_Message">[The <b>MethodContext</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>MethodContext</b> class is the pointer to a structure used in a provider to get or set <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">MethodContext</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>MethodContext</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc68eddb-7991-42bd-bc0e-4f5d890ca468">GetStatusObject</a>
</td>
<td align="left" width="63%">
Gets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fe1f1af-61a9-490b-95e0-c3a3efe2392d">SetStatusObject</a>
</td>
<td align="left" width="63%">
Sets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

</td>
</tr>
</table> 


## -members

The <b>MethodContext</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc68eddb-7991-42bd-bc0e-4f5d890ca468">GetStatusObject</a>
</td>
<td align="left" width="63%">
Gets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fe1f1af-61a9-490b-95e0-c3a3efe2392d">SetStatusObject</a>
</td>
<td align="left" width="63%">
Sets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

</td>
</tr>
</table>Gets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

Sets an internal pointer to <a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

 


## -remarks



The destructor for this class is <b>MethodContext::~MethodContext</b>.




## -see-also




<a href="https://msdn.microsoft.com/d2414a72-3435-4035-bcd9-b3ec87f5709c">Provider Framework Utility Classes</a>
 

 


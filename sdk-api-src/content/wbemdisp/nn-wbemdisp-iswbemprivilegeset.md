---
UID: NN:wbemdisp.ISWbemPrivilegeSet
title: ISWbemPrivilegeSet
author: windows-sdk-content
description: An SWbemPrivilegeSet object is a collection of SWbemPrivilege objects in an SWbemSecurity object that requests specific privileges for a Windows Management Instrumentation (WMI) object.
old-location: wmi\swbemprivilegeset.htm
old-project: WmiSdk
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemPrivilegeSet, SWbemPrivilegeSet, SWbemPrivilegeSet object [Windows Management Instrumentation], SWbemPrivilegeSet object [Windows Management Instrumentation],described, _hmm_swbemprivilegeset, wbemdisp/SWbemPrivilegeSet, wmi.swbemprivilegeset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemPrivilegeSet
 - ISWbemPrivilegeSet
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemPrivilegeSet interface


## -description


An 
<b>SWbemPrivilegeSet</b> object is a collection of 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> objects in an 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> object that requests specific privileges for a Windows Management Instrumentation (WMI) object. See the list of privileges in <a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>. Items are added to the collection using the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a> and 
<a href="https://msdn.microsoft.com/729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1">AddAsString</a> methods.  Items are retrieved from the collection using the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> method, and removed using the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a> method. This object cannot be created by the VBScript <a href="https://msdn.microsoft.com/en-us/library/xzysf6hc(v=vs.84).aspx">CreateObject</a> method call. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>.

An 
<b>SWbemPrivilegeSet</b> object is a set of privilege override requests for a specific  object. When an API call is made using this object, the privilege override requests are attempted. The  
<b>SWbemPrivilegeSet</b> object does not define the privileges available to the current user or process. In other words, obtaining the privileges for any WMI object does not identify the   privilege settings that are made on the connection to WMI,  or the privileges in effect when an object is delivered to a sink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemPrivilegeSet</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemPrivilegeSet</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object to the 
<b>SWbemPrivilegeSet</b> collection using a 
<a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a> constant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1">AddAsString</a>
</td>
<td align="left" width="63%">
Adds an 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object to the 
<b>SWbemPrivilegeSet</b> collection using a privilege string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/368caa14-1c53-4090-8569-97ea743905de">DeleteAll</a>
</td>
<td align="left" width="63%">
Deletes all the privileges from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Retrieves an 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object from the collection. This is the default method of this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> object from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemPrivilegeSet</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of items in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/11bb8723-f329-4083-8219-2256ce44a5e3">Executing Privileged Operations</a>



<a href="https://msdn.microsoft.com/65b923d5-5244-498d-9644-d4978fb84f85">Executing Privileged Operations Using VBScript</a>



<a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>



<a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a>
 

 


---
UID: NN:wbemdisp.ISWbemObjectPath
title: ISWbemObjectPath
author: windows-sdk-content
description: Use the methods and properties of the SWbemObjectPath object to construct and validate an object path. This object can be created by the VBScript CreateObject call.
old-location: wmi\swbemobjectpath.htm
old-project: WmiSdk
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemObjectPath, SWbemObjectPath, SWbemObjectPath object [Windows Management Instrumentation], SWbemObjectPath object [Windows Management Instrumentation],described, _hmm_swbemobjectpath, wbemdisp/SWbemObjectPath, wmi.swbemobjectpath
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
 - SWbemObjectPath
 - ISWbemObjectPath
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObjectPath interface


## -description


Use the methods and properties of the 
<b>SWbemObjectPath</b> object to construct and validate an object path. This object can be created by the VBScript <b>CreateObject</b> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObjectPath</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemObjectPath</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d341b980-bac9-4db4-a55f-eb971fb385da">SetAsClass</a>
</td>
<td align="left" width="63%">
Forces the path to address a WMI class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ec53954-2aac-494c-87c7-6a14592d8bd5">SetAsSingleton</a>
</td>
<td align="left" width="63%">
Forces the path to address a singleton WMI instance.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObjectPath</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f00e5759-03b4-4333-b89e-5f54db73c3b7">Authority</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
String that defines the Authority component of the object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/60123963-31be-4112-9d06-611b4c599fd4">Class</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Name of the class that is part of the object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">DisplayName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
String that contains the path in a form that can be used as a moniker display name. See 
<a href="https://msdn.microsoft.com/c0d18827-6b36-4817-8cd9-06cd0f267b28">Creating a WMI Application or Script</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/55d50785-6cdb-4e42-8b59-121f339494df">IsClass</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Boolean value that indicates if this path represents a class. This is analogous to the 
<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">__Genus</a> property in the COM API.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0d0533be-89fe-4ab6-bafa-2da6195ff02c">IsSingleton</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Boolean value that indicates if this path represents a singleton instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1919403d-6dea-4d41-9bc7-a622a9c9c2c8">Keys</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that contains the key value bindings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cde4ebac-b112-48b5-a274-802e6d3fbfbf">Locale</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
String that contains the locale for this object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/be88670d-6f0d-4b9d-886f-3e70bf4758ed">Namespace</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Name of the namespace that is part of the object path. This is the same as the 
<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">__Namespace</a> property in the COM API.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/506cf172-2c8b-48fe-bcdd-572bdca754a8">ParentNamespace</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the parent of the namespace that is part of the object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915708">Path</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Contains the absolute path. This is the same as the 
<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">__Path</a> system property in the COM API. This is the default property of this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b">Relpath</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Contains the relative path. This is the same as the 
<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">__Relpath</a> system property in the COM API.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/26e5e990-3b78-41b6-83c4-ba0d8b0d2f00">Security_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Used to read or change the security settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8d711bc5-dd5e-426f-8398-38f90655ff75">Server</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Name of the server. This is the same as the 
<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">__Server</a> system property in the COM API.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 


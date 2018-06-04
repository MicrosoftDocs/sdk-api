---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# INetFwAuthorizedApplication interface


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

The <b>INetFwAuthorizedApplication</b> interface provides access to the properties of an application that has been authorized have openings in the firewall.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwAuthorizedApplication</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>INetFwAuthorizedApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>INetFwAuthorizedApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03a1503e-aee5-484f-8a4c-a7e10dffe401">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the     Enabled property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0a4127f-4f81-4b71-a5c5-ba9e30927820">get_IpVersion</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the    IpVersion property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4937e0a5-089f-404f-b0dc-bba8e8a332a5">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the  Name property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14e7c8e1-088c-4eae-8f93-7ee41bfa484b">get_ProcessImageFileName</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the ProcessImageFileName property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56e51590-8cde-4c7d-8034-bc13f16f2617">get_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the RemoteAddresses property for this  application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ba9e6d1-82a4-4a58-9da0-0e07e79b0030">get_Scope</a>
</td>
<td align="left" width="63%">
Retrieves the contents of the Scope property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03a1503e-aee5-484f-8a4c-a7e10dffe401">put_Enabled</a>
</td>
<td align="left" width="63%">
Sets the contents of the     Enabled property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0a4127f-4f81-4b71-a5c5-ba9e30927820">put_IpVersion</a>
</td>
<td align="left" width="63%">
Sets the contents of the    IpVersion property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4937e0a5-089f-404f-b0dc-bba8e8a332a5">put_Name</a>
</td>
<td align="left" width="63%">
Sets the contents of the  Name property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14e7c8e1-088c-4eae-8f93-7ee41bfa484b">put_ProcessImageFileName</a>
</td>
<td align="left" width="63%">
Sets the contents of the ProcessImageFileName property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56e51590-8cde-4c7d-8034-bc13f16f2617">put_RemoteAddresses</a>
</td>
<td align="left" width="63%">
Sets the contents of the RemoteAddresses property for this  application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ba9e6d1-82a4-4a58-9da0-0e07e79b0030">put_Scope</a>
</td>
<td align="left" width="63%">
Sets the contents of the Scope property.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INetFwAuthorizedApplication</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a>


</td>
<td align="left" width="63%">
Accesses the  Enabled property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f0a4127f-4f81-4b71-a5c5-ba9e30927820">IpVersion</a>


</td>
<td align="left" width="63%">
Accesses the IpVersion property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="63%">
Accesses the Name property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/14e7c8e1-088c-4eae-8f93-7ee41bfa484b">ProcessImageFileName</a>


</td>
<td align="left" width="63%">
Accesses the ProcessImageFileName property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/56e51590-8cde-4c7d-8034-bc13f16f2617">RemoteAddresses</a>


</td>
<td align="left" width="63%">
Accesses the RemoteAddresses property for this application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915814">Scope</a>


</td>
<td align="left" width="63%">
Accesses the contents of the Scope property.

</td>
</tr>
</table> 


## -remarks



When creating new applications, this interface is supported by the HNetCfg.FwAuthorizedApplication COM object.  

For reading or modifying existing applications, instances of this interface are retrieved through the <a href="https://msdn.microsoft.com/70ea2cd1-5422-4db1-ab84-9924dab5623d">INetFwAuthorizedApplications</a> collection.

All configuration changes take effect immediately.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/70ea2cd1-5422-4db1-ab84-9924dab5623d">INetFwAuthorizedApplications</a>



<a href="_com_iunknown">IUnknown</a>
 

 


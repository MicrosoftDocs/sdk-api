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

# IEnumWIA_DEV_CAPS interface


## -description


The <b>IEnumWIA_DEV_CAPS</b> interface enumerates the currently available Windows Image Acquisition (WIA) hardware device capabilities. Device capabilities include commands and events that the device supports.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWIA_DEV_CAPS</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumWIA_DEV_CAPS</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWIA_DEV_CAPS</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/00129d58-d3e1-46c3-9dad-3787fafc2ba7">IEnumWIA_DEV_CAPS::Clone</a> method creates an additional instance of the <b>IEnumWIA_DEV_CAPS</b> interface and sends back a pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c9418d1f-0890-4771-9641-5ea723449779">IEnumWIA_DEV_CAPS::GetCount</a> method returns the number of elements stored by this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a2d4bc7a-cf2c-4ac2-9ae4-43334ddcb171">IEnumWIA_DEV_CAPS::Next</a> method fills an array of pointers to <a href="https://msdn.microsoft.com/9bf123c7-234f-45d3-bb45-c0cb135ef970">WIA_DEV_CAP</a> structures.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c5a3239d-f60d-4bff-b788-155286e97545">IEnumWIA_DEV_CAPS::Reset</a> method is used by applications to restart the enumeration of device capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/172f9ba6-5ca8-4d42-ba6b-5e9e5606b67d">IEnumWIA_DEV_CAPS::Skip</a> method skips the specified number of hardware device capabilities during an enumeration of available device capabilities.


</td>
</tr>
</table> 


## -remarks



The <b>IEnumWIA_DEV_CAPS</b> interface is a specific implementation for WIA of the standard OLE enumeration interface. For details, see <a href="_com_ienumxxxx">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWIA_DEV_CAPS</b> interface by invoking the <a href="https://msdn.microsoft.com/3a54ce9b-d266-4ab2-8256-cd8cf76d6b2f">IWiaItem::EnumDeviceCapabilities</a> method.

The <b>IEnumWIA_DEV_CAPS</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods.

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a54ce9b-d266-4ab2-8256-cd8cf76d6b2f">EnumDeviceCapabilities</a>



<a href="_com_ienumxxxx">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>
 

 


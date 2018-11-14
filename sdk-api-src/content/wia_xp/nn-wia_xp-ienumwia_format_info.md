---
UID: NN:wia_xp.IEnumWIA_FORMAT_INFO
title: IEnumWIA_FORMAT_INFO
author: windows-sdk-content
description: Use the IEnumWIA_FORMAT_INFO interface to enumerate the format and media type information for a device.
old-location: wia\_wia_IEnumWIA_FORMAT_INFO.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_format_info\ienumwia_format_info.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumWIA_FORMAT_INFO, IEnumWIA_FORMAT_INFO interface [WIA], IEnumWIA_FORMAT_INFO interface [WIA],described, _wia_IEnumWIA_FORMAT_INFO, wia._wia_IEnumWIA_FORMAT_INFO, wia_xp/IEnumWIA_FORMAT_INFO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IEnumWIA_FORMAT_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumWIA_FORMAT_INFO interface


## -description


Use the <b>IEnumWIA_FORMAT_INFO</b> interface to enumerate the format and media type information for a device.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWIA_FORMAT_INFO</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumWIA_FORMAT_INFO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWIA_FORMAT_INFO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629830(v=VS.85).aspx">Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629830(v=VS.85).aspx">IEnumWIA_FORMAT_INFO::Clone</a> method creates an additional instance of the <b>IEnumWIA_FORMAT_INFO</b> interface and returns an interface pointer to the new interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629832(v=VS.85).aspx">GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629832(v=VS.85).aspx">IEnumWIA_FORMAT_INFO::GetCount</a> method returns the number of elements stored by this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630159(v=VS.85).aspx">Next</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630159(v=VS.85).aspx">IEnumWIA_FORMAT_INFO::Next</a> method returns an array of <a href="https://msdn.microsoft.com/en-us/library/ms629878(v=VS.85).aspx">WIA_FORMAT_INFO</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630160(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630160(v=VS.85).aspx">IEnumWIA_FORMAT_INFO::Reset</a> method sets the enumeration back to the first <a href="https://msdn.microsoft.com/en-us/library/ms629878(v=VS.85).aspx">WIA_FORMAT_INFO</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630161(v=VS.85).aspx">Skip</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630161(v=VS.85).aspx">IEnumWIA_FORMAT_INFO::Skip</a> method skips the specified number of structures in the enumeration.

</td>
</tr>
</table> 


## -remarks



The <b>IEnumWIA_FORMAT_INFO</b> interface is a specific implementation for Windows Image Acquisition (WIA) of the standard Component Object Model (COM) enumeration interface. For details, see <a href="https://msdn.microsoft.com/library/ms680089(v=VS.85).aspx">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWIA_FORMAT_INFO</b> interface by invoking the <a href="https://msdn.microsoft.com/en-us/library/ms630150(v=VS.85).aspx">IWiaDataTransfer::idtEnumWIA_FORMAT_INFO</a> method of an item's <a href="https://msdn.microsoft.com/en-us/library/ms630155(v=VS.85).aspx">IWiaDataTransfer</a> interface.

The <b>IEnumWIA_FORMAT_INFO</b> interface, like all COM interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

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




<a href="https://msdn.microsoft.com/library/ms680089(v=VS.85).aspx">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms630150(v=VS.85).aspx">idtEnumWIA_FORMAT_INFO</a>
 

 


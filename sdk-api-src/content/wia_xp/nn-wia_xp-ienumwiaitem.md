---
UID: NN:wia_xp.IEnumWiaItem
title: IEnumWiaItem
author: windows-sdk-content
description: The IEnumWiaItem interface is used by applications to enumerate IWiaItem objects in the tree's current folder.
old-location: wia\_wia_IEnumWiaItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwiaitem\ienumwiaitem.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnumWiaItem, IEnumWiaItem interface [WIA], IEnumWiaItem interface [WIA],described, _wia_IEnumWiaItem, wia._wia_IEnumWiaItem, wia_xp/IEnumWiaItem
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
 - IEnumWiaItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumWiaItem interface


## -description


The <b>IEnumWiaItem</b> interface is used by applications to enumerate <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> objects in the tree's current folder. The Windows Image Acquisition (WIA) run-time system represents every WIA hardware device to applications as a hierarchical tree of <b>IWiaItem</b> objects.

<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/en-us/library/ms630172(v=VS.85).aspx">IEnumWiaItem2</a> instead of <b>IEnumWiaItem</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWiaItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumWiaItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWiaItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629841(v=VS.85).aspx">IEnumWiaItem::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629841(v=VS.85).aspx">IEnumWiaItem::Clone</a> method creates an additional instance of the <b>IEnumWiaItem</b> interface and sends back a pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629842(v=VS.85).aspx">IEnumWiaItem::GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629842(v=VS.85).aspx">IEnumWiaItem::GetCount</a> method returns the number of elements stored by this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630177(v=VS.85).aspx">IEnumWiaItem::Next</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630177(v=VS.85).aspx">IEnumWiaItem::Next</a> method fills an array of pointers to <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630178(v=VS.85).aspx">IEnumWiaItem::Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630178(v=VS.85).aspx">IEnumWiaItem::Reset</a> method is used by applications to restart the enumeration of item information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630179(v=VS.85).aspx">IEnumWiaItem::Skip</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630179(v=VS.85).aspx">IEnumWiaItem::Skip</a> method skips the specified number of items during an enumeration of available <a href="https://msdn.microsoft.com/en-us/library/ms630113(v=VS.85).aspx">IWiaItem</a> objects.

</td>
</tr>
</table> 


## -remarks



The <b>IEnumWiaItem</b> interface is a specific implementation for WIA of the standard Component Object Model (COM) enumeration interface. For details, see <a href="https://msdn.microsoft.com/library/ms680089(v=VS.85).aspx">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWiaItem</b> interface by invoking the <a href="https://msdn.microsoft.com/en-us/library/ms630101(v=VS.85).aspx">IWiaItem::EnumChildItems</a> method.

The <b>IEnumWiaItem</b> interface, like all COM interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

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




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms630101(v=VS.85).aspx">EnumChildItems</a>



<a href="https://msdn.microsoft.com/en-us/library/ms629850(v=VS.85).aspx">Enumerating Items</a>



<a href="https://msdn.microsoft.com/library/ms680089(v=VS.85).aspx">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>
 

 


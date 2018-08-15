---
UID: NN:wia_xp.IEnumWiaItem
title: IEnumWiaItem
author: windows-sdk-content
description: The IEnumWiaItem interface is used by applications to enumerate IWiaItem objects in the tree's current folder.
old-location: wia\_wia_IEnumWiaItem.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwiaitem\ienumwiaitem.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEnumWiaItem, IEnumWiaItem interface [WIA], IEnumWiaItem interface [WIA],described, _wia_IEnumWiaItem, wia._wia_IEnumWiaItem, wia_xp/IEnumWiaItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wia_xp.h
req.include-header: Wia.h
req.redist: 
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
tech.root: 
req.typenames: WIAVIDEO_STATE
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
req.lib: Wiaguid.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWiaItem interface


## -description


The <b>IEnumWiaItem</b> interface is used by applications to enumerate <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects in the tree's current folder. The Windows Image Acquisition (WIA) run-time system represents every WIA hardware device to applications as a hierarchical tree of <b>IWiaItem</b> objects.

<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/a82298e0-fbe7-4ef5-99c5-18ff60538e03">IEnumWiaItem2</a> instead of <b>IEnumWiaItem</b>.</div><div> </div>

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
<a href="https://msdn.microsoft.com/5c1bebde-fdd7-4446-9750-2ac50b4c113a">IEnumWiaItem::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/5c1bebde-fdd7-4446-9750-2ac50b4c113a">IEnumWiaItem::Clone</a> method creates an additional instance of the <b>IEnumWiaItem</b> interface and sends back a pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75c2ab78-6803-4cfc-bc40-936554aff12e">IEnumWiaItem::GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/75c2ab78-6803-4cfc-bc40-936554aff12e">IEnumWiaItem::GetCount</a> method returns the number of elements stored by this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aec38b89-9d67-4963-876f-d4d43cc557f1">IEnumWiaItem::Next</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/aec38b89-9d67-4963-876f-d4d43cc557f1">IEnumWiaItem::Next</a> method fills an array of pointers to <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/944bf74c-4c2b-4147-9f18-84f493b59a4d">IEnumWiaItem::Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/944bf74c-4c2b-4147-9f18-84f493b59a4d">IEnumWiaItem::Reset</a> method is used by applications to restart the enumeration of item information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec703316-3623-4ce3-a9e0-aa3768285aba">IEnumWiaItem::Skip</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ec703316-3623-4ce3-a9e0-aa3768285aba">IEnumWiaItem::Skip</a> method skips the specified number of items during an enumeration of available <a href="https://msdn.microsoft.com/b9aaf7ae-7222-44d1-8cf1-89234b263135">IWiaItem</a> objects.

</td>
</tr>
</table> 


## -remarks



The <b>IEnumWiaItem</b> interface is a specific implementation for WIA of the standard Component Object Model (COM) enumeration interface. For details, see <a href="_com_ienumxxxx">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWiaItem</b> interface by invoking the <a href="https://msdn.microsoft.com/cc03659a-6718-4654-b8c5-881dbec95ce0">IWiaItem::EnumChildItems</a> method.

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



<a href="https://msdn.microsoft.com/cc03659a-6718-4654-b8c5-881dbec95ce0">EnumChildItems</a>



<a href="https://msdn.microsoft.com/ab7246e8-47bb-4b94-8d91-1c22010ebd9f">Enumerating Items</a>



<a href="_com_ienumxxxx">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>
 

 


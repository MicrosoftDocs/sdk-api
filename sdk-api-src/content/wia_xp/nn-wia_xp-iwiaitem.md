---
UID: NN:wia_xp.IWiaItem
title: IWiaItem
author: windows-sdk-content
description: Each Windows Image Acquisition (WIA) hardware device is represented to an application as a hierarchical tree of IWiaItem objects.
old-location: wia\_wia_IWiaItem.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\iwiaitem.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWiaItem, IWiaItem interface [WIA], IWiaItem interface [WIA],described, _wia_IWiaItem, wia._wia_IWiaItem, wia_xp/IWiaItem
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaItem
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaItem interface


## -description


Each Windows Image Acquisition (WIA) hardware device is represented to an application as a hierarchical tree of <b>IWiaItem</b> objects. The <b>IWiaItem</b> interface provides applications with the ability to query devices to discover their capabilities. It also provides access to data transfer interfaces and item properties. In addition, the <b>IWiaItem</b> interface provides methods to enable applications to control the device.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/4e29ea54-1ee7-4150-b26c-f8c7f41a3f08">IWiaItem2</a> instead of <b>IWiaItem</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0877ca9d-555f-4ffe-9926-20af13563be6">AnalyzeItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0877ca9d-555f-4ffe-9926-20af13563be6">IWiaItem::AnalyzeItem</a> method causes the WIA hardware device to acquire and try to detect what data types are present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b01a932b-1f11-49bf-941e-ec118b0ffb5c">CreateChildItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b01a932b-1f11-49bf-941e-ec118b0ffb5c">IWiaItem::CreateChildItem</a> method is used by applications to add <b>IWiaItem</b> objects to the <b>IWiaItem</b> tree of a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/355021f3-7a5f-4a3f-bd08-cc85514ae6a2">DeleteItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/355021f3-7a5f-4a3f-bd08-cc85514ae6a2">IWiaItem::DeleteItem</a> method removes the current <b>IWiaItem</b> object from the object tree of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9403cae-9437-4ef1-bf9b-f0ac77cbe3cb">DeviceCommand</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e9403cae-9437-4ef1-bf9b-f0ac77cbe3cb">IWiaItem::DeviceCommand</a> issues a command to a WIA hardware device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3a337d3-4fcb-4cb7-aa0a-b9fa18a0415a">DeviceDlg</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/d3a337d3-4fcb-4cb7-aa0a-b9fa18a0415a">IWiaItem::DeviceDlg</a> method is used by applications to display a dialog box to the user to prepare for image acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/565e8787-cec3-4965-a810-bb4f46f1a156">Diagnostic</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d0991d7-0a18-43ae-a7e8-9db27c0fbac4">DumpDrvItemData</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5d7f9a5-3117-405e-b38d-5c5030b553db">DumpItemData</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01242c56-86ba-4fe4-aa43-dc06457dcb0c">DumpTreeItemData</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc03659a-6718-4654-b8c5-881dbec95ce0">EnumChildItems</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cc03659a-6718-4654-b8c5-881dbec95ce0">IWiaItem::EnumChildItems</a> method creates an enumerator object and passes back a pointer to its <a href="https://msdn.microsoft.com/25eab463-a531-4cb7-b8b7-6b1c8d060ee8">IEnumWiaItem</a> interface for non-empty folders in a <b>IWiaItem</b> tree of a WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a54ce9b-d266-4ab2-8256-cd8cf76d6b2f">EnumDeviceCapabilities</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3a54ce9b-d266-4ab2-8256-cd8cf76d6b2f">IWiaItem::EnumDeviceCapabilities</a> method creates an enumerator that is used to ascertain the commands and events a WIA device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb35f225-3831-4442-b1e7-6314f59d158a">EnumRegisterEventInfo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fb35f225-3831-4442-b1e7-6314f59d158a">IWiaItem::EnumRegisterEventInfo</a> method creates an enumerator used to obtain information about events for which an application is registered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23bbfc74-1f92-4776-a432-7a3ce25e3454">FindItemByName</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/23bbfc74-1f92-4776-a432-7a3ce25e3454">IWiaItem::FindItemByName</a> method searches an item's tree of sub-items using the name as the search key. Each <b>IWiaItem</b> object has a name as one of its standard properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ef84150-ecd7-4f4c-9320-e65aa5e06ed5">GetItemType</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2ef84150-ecd7-4f4c-9320-e65aa5e06ed5">IWiaItem::GetItemType</a> method is called by applications to obtain the type information of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddae70df-bf96-4f55-8fe6-373c6a485529">GetRootItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/ddae70df-bf96-4f55-8fe6-373c6a485529">IWiaItem::GetRootItem</a> method retrieves the root item of a tree of item objects used to represent a WIA hardware device.

</td>
</tr>
</table> 


## -remarks



Some of the methods of the <b>IWiaItem</b> interface are valid only on the root item of the device's tree. Other methods are valid on all items. The methods are grouped as follows:

<table class="clsStd">
<tr>
<td>Valid On Root Item Only</td>
<td>
<a href="https://msdn.microsoft.com/e9403cae-9437-4ef1-bf9b-f0ac77cbe3cb">IWiaItem::DeviceCommand</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/d3a337d3-4fcb-4cb7-aa0a-b9fa18a0415a">IWiaItem::DeviceDlg</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/3a54ce9b-d266-4ab2-8256-cd8cf76d6b2f">IWiaItem::EnumDeviceCapabilities</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/fb35f225-3831-4442-b1e7-6314f59d158a">IWiaItem::EnumRegisterEventInfo</a>
</td>
</tr>
<tr>
<td>Valid On All Items</td>
<td>
<a href="https://msdn.microsoft.com/0877ca9d-555f-4ffe-9926-20af13563be6">IWiaItem::AnalyzeItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/b01a932b-1f11-49bf-941e-ec118b0ffb5c">IWiaItem::CreateChildItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/355021f3-7a5f-4a3f-bd08-cc85514ae6a2">IWiaItem::DeleteItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/cc03659a-6718-4654-b8c5-881dbec95ce0">IWiaItem::EnumChildItems</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/23bbfc74-1f92-4776-a432-7a3ce25e3454">IWiaItem::FindItemByName</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/2ef84150-ecd7-4f4c-9320-e65aa5e06ed5">IWiaItem::GetItemType</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/ddae70df-bf96-4f55-8fe6-373c6a485529">IWiaItem::GetRootItem</a>
</td>
</tr>
</table>
 

The <b>IWiaItem</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

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
 




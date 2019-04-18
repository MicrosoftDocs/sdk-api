---
UID: NN:wia_xp.IWiaItem
title: IWiaItem (wia_xp.h)
author: windows-sdk-content
description: Each Windows Image Acquisition (WIA) hardware device is represented to an application as a hierarchical tree of IWiaItem objects.
old-location: wia\_wia_IWiaItem.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiaitem\iwiaitem.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWiaItem, IWiaItem interface [WIA], IWiaItem interface [WIA],described, _wia_IWiaItem, wia._wia_IWiaItem, wia_xp/IWiaItem
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
req.dll: Wiaservc.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWiaItem interface


## -description


Each Windows Image Acquisition (WIA) hardware device is represented to an application as a hierarchical tree of <b>IWiaItem</b> objects. The <b>IWiaItem</b> interface provides applications with the ability to query devices to discover their capabilities. It also provides access to data transfer interfaces and item properties. In addition, the <b>IWiaItem</b> interface provides methods to enable applications to control the device.
<div class="alert"><b>Note</b>  For Windows Vista applications, use <a href="https://msdn.microsoft.com/en-us/library/ms629989(v=VS.85).aspx">IWiaItem2</a> instead of <b>IWiaItem</b>.</div><div> </div>

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
<a href="https://msdn.microsoft.com/en-us/library/ms630010(v=VS.85).aspx">AnalyzeItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630010(v=VS.85).aspx">IWiaItem::AnalyzeItem</a> method causes the WIA hardware device to acquire and try to detect what data types are present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630011(v=VS.85).aspx">CreateChildItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630011(v=VS.85).aspx">IWiaItem::CreateChildItem</a> method is used by applications to add <b>IWiaItem</b> objects to the <b>IWiaItem</b> tree of a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630012(v=VS.85).aspx">DeleteItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630012(v=VS.85).aspx">IWiaItem::DeleteItem</a> method removes the current <b>IWiaItem</b> object from the object tree of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630013(v=VS.85).aspx">DeviceCommand</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630013(v=VS.85).aspx">IWiaItem::DeviceCommand</a> issues a command to a WIA hardware device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630014(v=VS.85).aspx">DeviceDlg</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630014(v=VS.85).aspx">IWiaItem::DeviceDlg</a> method is used by applications to display a dialog box to the user to prepare for image acquisition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630015(v=VS.85).aspx">Diagnostic</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630016(v=VS.85).aspx">DumpDrvItemData</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630098(v=VS.85).aspx">DumpItemData</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630100(v=VS.85).aspx">DumpTreeItemData</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630101(v=VS.85).aspx">EnumChildItems</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630101(v=VS.85).aspx">IWiaItem::EnumChildItems</a> method creates an enumerator object and passes back a pointer to its <a href="https://msdn.microsoft.com/en-us/library/ms630176(v=VS.85).aspx">IEnumWiaItem</a> interface for non-empty folders in a <b>IWiaItem</b> tree of a WIA device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630103(v=VS.85).aspx">EnumDeviceCapabilities</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630103(v=VS.85).aspx">IWiaItem::EnumDeviceCapabilities</a> method creates an enumerator that is used to ascertain the commands and events a WIA device supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630105(v=VS.85).aspx">EnumRegisterEventInfo</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630105(v=VS.85).aspx">IWiaItem::EnumRegisterEventInfo</a> method creates an enumerator used to obtain information about events for which an application is registered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630107(v=VS.85).aspx">FindItemByName</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630107(v=VS.85).aspx">IWiaItem::FindItemByName</a> method searches an item's tree of sub-items using the name as the search key. Each <b>IWiaItem</b> object has a name as one of its standard properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630108(v=VS.85).aspx">GetItemType</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630108(v=VS.85).aspx">IWiaItem::GetItemType</a> method is called by applications to obtain the type information of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630110(v=VS.85).aspx">GetRootItem</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630110(v=VS.85).aspx">IWiaItem::GetRootItem</a> method retrieves the root item of a tree of item objects used to represent a WIA hardware device.

</td>
</tr>
</table> 


## -remarks



Some of the methods of the <b>IWiaItem</b> interface are valid only on the root item of the device's tree. Other methods are valid on all items. The methods are grouped as follows:

<table class="clsStd">
<tr>
<td>Valid On Root Item Only</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630013(v=VS.85).aspx">IWiaItem::DeviceCommand</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630014(v=VS.85).aspx">IWiaItem::DeviceDlg</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630103(v=VS.85).aspx">IWiaItem::EnumDeviceCapabilities</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630105(v=VS.85).aspx">IWiaItem::EnumRegisterEventInfo</a>
</td>
</tr>
<tr>
<td>Valid On All Items</td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630010(v=VS.85).aspx">IWiaItem::AnalyzeItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630011(v=VS.85).aspx">IWiaItem::CreateChildItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630012(v=VS.85).aspx">IWiaItem::DeleteItem</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630101(v=VS.85).aspx">IWiaItem::EnumChildItems</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630107(v=VS.85).aspx">IWiaItem::FindItemByName</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630108(v=VS.85).aspx">IWiaItem::GetItemType</a>
</td>
</tr>
<tr>
<td> </td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/ms630110(v=VS.85).aspx">IWiaItem::GetRootItem</a>
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
 




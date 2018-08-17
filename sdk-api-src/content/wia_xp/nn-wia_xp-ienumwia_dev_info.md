---
UID: NN:wia_xp.IEnumWIA_DEV_INFO
title: IEnumWIA_DEV_INFO
author: windows-sdk-content
description: The IEnumWIA_DEV_INFO interface enumerates the currently available Windows Image Acquisition (WIA) hardware devices and their properties. Device information properties describe the installation and configuration of WIA hardware devices.
old-location: wia\_wia_IEnumWIA_DEV_INFO.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_dev_info\ienumwia_dev_info.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEnumWIA_DEV_INFO, IEnumWIA_DEV_INFO interface [WIA], IEnumWIA_DEV_INFO interface [WIA],described, _wia_IEnumWIA_DEV_INFO, wia._wia_IEnumWIA_DEV_INFO, wia_xp/IEnumWIA_DEV_INFO
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
 - IEnumWIA_DEV_INFO
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWIA_DEV_INFO interface


## -description


The <b>IEnumWIA_DEV_INFO</b> interface enumerates the currently available Windows Image Acquisition (WIA) hardware devices and their properties. Device information properties describe the installation and configuration of WIA hardware devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWIA_DEV_INFO</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumWIA_DEV_INFO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWIA_DEV_INFO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629833(v=VS.85).aspx">Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629833(v=VS.85).aspx">IEnumWIA_DEV_INFO::Clone</a> method creates an additional instance of the <b>IEnumWIA_DEV_INFO</b> interface and sends back a pointer to it.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms629835(v=VS.85).aspx">GetCount</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms629835(v=VS.85).aspx">IEnumWIA_DEV_INFO::GetCount</a> method returns the number of elements stored by this enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630163(v=VS.85).aspx">Next</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630163(v=VS.85).aspx">IEnumWIA_DEV_INFO::Next</a> method fills an array of pointers to <a href="https://msdn.microsoft.com/en-us/library/ms629938(v=VS.85).aspx">IWiaPropertyStorage</a> interfaces.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630164(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630164(v=VS.85).aspx">IEnumWIA_DEV_INFO::Reset</a> method is used by applications to restart the enumeration of device information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms630165(v=VS.85).aspx">Skip</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms630165(v=VS.85).aspx">IEnumWIA_DEV_INFO::Skip</a> method skips the specified number of hardware devices during an enumeration of available devices.

</td>
</tr>
</table> 


## -remarks



The <b>IEnumWIA_DEV_INFO</b> interface is a specific implementation for WIA of the standard OLE enumeration interface. For details, see <a href="https://msdn.microsoft.com/library/ms680089(v=VS.85).aspx">IEnumXXXX</a>.

Applications obtain a pointer to the <b>IEnumWIA_DEV_INFO</b> interface by invoking the <a href="https://msdn.microsoft.com/en-us/library/ms630142(v=VS.85).aspx">IWiaDevMgr::EnumDeviceInfo</a> method.

The <b>IEnumWIA_DEV_INFO</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface methods. 

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



<a href="https://msdn.microsoft.com/en-us/library/ms630142(v=VS.85).aspx">EnumDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms629852(v=VS.85).aspx">Enumerating System Devices</a>



<a href="https://msdn.microsoft.com/library/ms680089(v=VS.85).aspx">IEnumXXXX</a>



<b>Other Resources</b>



<b>Reference</b>
 

 


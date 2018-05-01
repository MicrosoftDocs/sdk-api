---
UID: NN:mswmdm.IWMDeviceManager
title: IWMDeviceManager
author: windows-driver-content
description: The IWMDeviceManager interface is the top level Windows Media Device Manager interface for applications.
old-location: wmdm\iwmdevicemanager.htm
old-project: WMDM
ms.assetid: cac68821-42fc-4833-bf2e-eec1768869e6
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IWMDeviceManager, IWMDeviceManager interface [windows Media Device Manager], IWMDeviceManager interface [windows Media Device Manager], described, IWMDeviceManagerInterface, mswmdm/IWMDeviceManager, wmdm.iwmdevicemanager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IWMDeviceManager
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IWMDeviceManager interface


## -description



The <b>IWMDeviceManager</b> interface is the top level Windows Media Device Manager interface for applications. This is the first interface accessed by an application, and is used to acquire the <a href="https://msdn.microsoft.com/fcb93d2a-2107-4aa9-9b3a-130044d7dc96">IWMDMEnumDevice</a> interface used to enumerate the connected devices. This interface is obtained by calling <b>QueryInterface</b> on the authenticated <a href="https://msdn.microsoft.com/5da66dc2-825d-4332-b1cb-2b9d0fabb445">IComponentAuthenticate</a> interface. If the device supports it, use <a href="https://msdn.microsoft.com/ea4bf623-c93a-4c0f-a84f-e3a979b37d60">IWMDeviceManager2</a> interface, which offers superior device enumeration capabilities.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDeviceManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDeviceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDeviceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1daa6d36-9858-4504-a9a2-c0341031829b">EnumDevices</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IWMDMEnumDevice</b> interface that can be used to enumerate portable devices connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efa8ccf6-c796-4ed7-8fe0-2e6570292aaa">GetDeviceCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of portable devices that are currently connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ecb84cc-eaa5-436c-b5f1-50705462b88b">GetRevision</a>
</td>
<td align="left" width="63%">
Retrieves the version number of Windows Media Device Manager currently in use.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ea4bf623-c93a-4c0f-a84f-e3a979b37d60">IWMDeviceManager2 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 


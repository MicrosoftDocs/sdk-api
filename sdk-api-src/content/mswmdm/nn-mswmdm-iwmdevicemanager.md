---
UID: NN:mswmdm.IWMDeviceManager
title: IWMDeviceManager (mswmdm.h)
description: The IWMDeviceManager interface is the top level Windows Media Device Manager interface for applications.
helpviewer_keywords: ["IWMDeviceManager","IWMDeviceManager interface [windows Media Device Manager]","IWMDeviceManager interface [windows Media Device Manager]","described","IWMDeviceManagerInterface","mswmdm/IWMDeviceManager","wmdm.iwmdevicemanager"]
old-location: wmdm\iwmdevicemanager.htm
tech.root: WMDM
ms.assetid: cac68821-42fc-4833-bf2e-eec1768869e6
ms.date: 12/05/2018
ms.keywords: IWMDeviceManager, IWMDeviceManager interface [windows Media Device Manager], IWMDeviceManager interface [windows Media Device Manager],described, IWMDeviceManagerInterface, mswmdm/IWMDeviceManager, wmdm.iwmdevicemanager
f1_keywords:
- mswmdm/IWMDeviceManager
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mswmdm.h
api_name:
- IWMDeviceManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDeviceManager interface


## -description



The <b>IWMDeviceManager</b> interface is the top level Windows Media Device Manager interface for applications. This is the first interface accessed by an application, and is used to acquire the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice">IWMDMEnumDevice</a> interface used to enumerate the connected devices. This interface is obtained by calling <b>QueryInterface</b> on the authenticated <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate">IComponentAuthenticate</a> interface. If the device supports it, use <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2">IWMDeviceManager2</a> interface, which offers superior device enumeration capabilities.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDeviceManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDeviceManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices">EnumDevices</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IWMDMEnumDevice</b> interface that can be used to enumerate portable devices connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-getdevicecount">GetDeviceCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of portable devices that are currently connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-getrevision">GetRevision</a>
</td>
<td align="left" width="63%">
Retrieves the version number of Windows Media Device Manager currently in use.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2">IWMDeviceManager2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 


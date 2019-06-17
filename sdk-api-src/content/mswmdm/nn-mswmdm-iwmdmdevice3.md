---
UID: NN:mswmdm.IWMDMDevice3
title: IWMDMDevice3 (mswmdm.h)
author: windows-sdk-content
description: The IWMDMDevice3 interface extends IWMDMDevice2 by providing methods to query a device for properties, send device I/O controle codes, and also providing upgraded methods to search for storages and retrieve device format capabilities.
old-location: wmdm\iwmdmdevice3.htm
tech.root: WMDM
ms.assetid: 29e0ec95-c1ea-4157-b5aa-39d80fff407d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMDevice3, IWMDMDevice3 interface [windows Media Device Manager], IWMDMDevice3 interface [windows Media Device Manager],described, IWMDMDevice3Interface, mswmdm/IWMDMDevice3, wmdm.iwmdmdevice3
ms.topic: interface
f1_keywords: ["mswmdm/IWMDMDevice3"]
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
 - IWMDMDevice3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMDevice3 interface


## -description



The <b>IWMDMDevice3</b> interface extends <b>IWMDMDevice2</b> by providing methods to query a device for properties, send device I/O controle codes, and also providing upgraded methods to search for storages and retrieve device format capabilities.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDevice3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2">IWMDMDevice2</a>. <b>IWMDMDevice3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMDevice3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol">DeviceIoControl</a>
</td>
<td align="left" width="63%">
Sends a Device I/O Control (IOCTL) code to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage">FindStorage</a>
</td>
<td align="left" width="63%">
Finds a storage by its persistent unique identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability">GetFormatCapability</a>
</td>
<td align="left" width="63%">
Retrieves device support for files of a specified format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves a specific device metadata property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a specific device property, if it is writable.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2">IWMDMDevice2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 


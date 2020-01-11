---
UID: NN:mswmdm.IWMDMDevice2
title: IWMDMDevice2 (mswmdm.h)
description: The IWMDMDevice2 interface extends IWMDMDevice by making it possible to get the video formats supported by a device, find storage from its name, and use property pages.
old-location: wmdm\iwmdmdevice2.htm
tech.root: WMDM
ms.assetid: d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9
ms.date: 12/05/2018
ms.keywords: IWMDMDevice2, IWMDMDevice2 interface [windows Media Device Manager], IWMDMDevice2 interface [windows Media Device Manager],described, IWMDMDevice2Interface, mswmdm/IWMDMDevice2, wmdm.iwmdmdevice2
f1_keywords:
- mswmdm/IWMDMDevice2
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
- IWMDMDevice2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMDevice2 interface


## -description



The <b>IWMDMDevice2</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice</a> by making it possible to get the video formats supported by a device, find storage from its name, and use property pages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDevice2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice</a>. <b>IWMDMDevice2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMDevice2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Retrieves the canonical name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2">GetFormatSupport2</a>
</td>
<td align="left" width="63%">
Retrieves the formats supported by the device, including audio and video codecs, and MIME file formats

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getspecifypropertypages">GetSpecifyPropertyPages</a>
</td>
<td align="left" width="63%">
Retrieves the property page for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getstorage">GetStorage</a>
</td>
<td align="left" width="63%">
Searches the immediate children of the root storage for a storage with the given name.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice">IWMDMDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3">IWMDMDevice3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 


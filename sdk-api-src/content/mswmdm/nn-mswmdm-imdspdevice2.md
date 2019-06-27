---
UID: NN:mswmdm.IMDSPDevice2
title: IMDSPDevice2 (mswmdm.h)
author: windows-sdk-content
description: The IMDSPDevice2 interface extends IMDSPDevice by getting extended formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name.
old-location: wmdm\imdspdevice2.htm
tech.root: WMDM
ms.assetid: a53052a1-89f4-4571-9eee-031e0049a92e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPDevice2, IMDSPDevice2 interface [windows Media Device Manager], IMDSPDevice2 interface [windows Media Device Manager],described, IMDSPDevice2Interface, mswmdm/IMDSPDevice2, wmdm.imdspdevice2
ms.topic: interface
f1_keywords: 
 - "mswmdm/IMDSPDevice2"
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
 - IMDSPDevice2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPDevice2 interface


## -description



The <b>IMDSPDevice2</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> by getting extended formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDevice2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a>. <b>IMDSPDevice2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPDevice2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice2-getcanonicalname">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Gets the name of a Plug and Play device. This method can return E_NOTIMPL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice2-getformatsupport2">GetFormatSupport2</a>
</td>
<td align="left" width="63%">
Gets the formats supported by a device, including audio and video formats, codecs, and MIME file formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice2-getspecifypropertypages">GetSpecifyPropertyPages</a>
</td>
<td align="left" width="63%">
Gets property pages of the portable device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice2-getstorage">GetStorage</a>
</td>
<td align="left" width="63%">
Returns a storage object from a storage name.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3">IMDSPDevice3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 


---
UID: NN:mswmdm.IMDSPDevice2
title: IMDSPDevice2
author: windows-sdk-content
description: The IMDSPDevice2 interface extends IMDSPDevice by getting extended formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name.
old-location: wmdm\imdspdevice2.htm
old-project: WMDM
ms.assetid: a53052a1-89f4-4571-9eee-031e0049a92e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMDSPDevice2, IMDSPDevice2 interface [windows Media Device Manager], IMDSPDevice2 interface [windows Media Device Manager],described, IMDSPDevice2Interface, mswmdm/IMDSPDevice2, wmdm.imdspdevice2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice2 interface


## -description



The <b>IMDSPDevice2</b> interface extends <a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a> by getting extended formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDevice2</b> interface inherits from <a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a>. <b>IMDSPDevice2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0888c780-e358-45ae-809b-34a19d496059">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Gets the name of a Plug and Play device. This method can return E_NOTIMPL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b05575b-5a43-4c12-a216-1b9f55742b6c">GetFormatSupport2</a>
</td>
<td align="left" width="63%">
Gets the formats supported by a device, including audio and video formats, codecs, and MIME file formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e79ce0d2-bfea-4a5b-82f8-9d69f96d9698">GetSpecifyPropertyPages</a>
</td>
<td align="left" width="63%">
Gets property pages of the portable device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d01cf5a6-1fdb-4354-8b43-b04bdc562d71">GetStorage</a>
</td>
<td align="left" width="63%">
Returns a storage object from a storage name.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>



<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 


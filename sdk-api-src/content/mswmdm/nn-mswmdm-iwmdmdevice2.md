---
UID: NN:mswmdm.IWMDMDevice2
title: IWMDMDevice2
author: windows-sdk-content
description: The IWMDMDevice2 interface extends IWMDMDevice by making it possible to get the video formats supported by a device, find storage from its name, and use property pages.
old-location: wmdm\iwmdmdevice2.htm
tech.root: WMDM
ms.assetid: d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWMDMDevice2, IWMDMDevice2 interface [windows Media Device Manager], IWMDMDevice2 interface [windows Media Device Manager],described, IWMDMDevice2Interface, mswmdm/IWMDMDevice2, wmdm.iwmdmdevice2
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDevice2 interface


## -description



The <b>IWMDMDevice2</b> interface extends <a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice</a> by making it possible to get the video formats supported by a device, find storage from its name, and use property pages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDevice2</b> interface inherits from <a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice</a>. <b>IWMDMDevice2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/16e18a9e-315f-41a2-b895-e3e478720864">GetCanonicalName</a>
</td>
<td align="left" width="63%">
Retrieves the canonical name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ace6192-5b50-40f0-98b4-5cab26a48798">GetFormatSupport2</a>
</td>
<td align="left" width="63%">
Retrieves the formats supported by the device, including audio and video codecs, and MIME file formats

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc46af60-5d74-4ac6-b680-c47b55c444e0">GetSpecifyPropertyPages</a>
</td>
<td align="left" width="63%">
Retrieves the property page for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17c7bb90-4c8c-4f1f-9b4c-41f31c5c5310">GetStorage</a>
</td>
<td align="left" width="63%">
Searches the immediate children of the root storage for a storage with the given name.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/44212da9-a38a-4ed5-86af-cf60b40bb54d">IWMDMDevice Interface</a>



<a href="https://msdn.microsoft.com/29e0ec95-c1ea-4157-b5aa-39d80fff407d">IWMDMDevice3 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 


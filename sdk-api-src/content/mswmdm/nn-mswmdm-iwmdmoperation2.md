---
UID: NN:mswmdm.IWMDMOperation2
title: IWMDMOperation2
author: windows-sdk-content
description: The optional, application-implemented IWMDMOperation2 interface extends IWMDMOperation by providing methods to get and set extended attributes.
old-location: wmdm\iwmdmoperation2.htm
tech.root: WMDM
ms.assetid: b3f7e92a-8feb-47cd-ae50-bc5bf9a37958
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMDMOperation2, IWMDMOperation2 interface [windows Media Device Manager], IWMDMOperation2 interface [windows Media Device Manager],described, IWMDMOperation2Interface, mswmdm/IWMDMOperation2, wmdm.iwmdmoperation2
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
 - IWMDMOperation2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMOperation2 interface


## -description



The optional, application-implemented <b>IWMDMOperation2</b> interface extends <a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation</a> by providing methods to get and set extended attributes.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMOperation2</b> interface inherits from <a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation</a>. <b>IWMDMOperation2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMOperation2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7bf76094-5660-47ac-b1a2-a67b6f95964b">GetObjectAttributes2</a>
</td>
<td align="left" width="63%">
Allows the application to specify attributes for an object being written to a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce19bfe5-c8ff-40f4-a152-8a46d2576c63">SetObjectAttributes2</a>
</td>
<td align="left" width="63%">
Sets attributes of files or storages. This method is currently not called by Windows Media Device Manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ff94191b-a0f2-4118-996c-d040f214fb9b">Handling File Transfers Manually</a>



<a href="https://msdn.microsoft.com/7277a8fe-3006-4456-b2e7-6041d3324f35">IWMDMOperation Interface</a>



<a href="https://msdn.microsoft.com/5ab4fdd2-d0bf-4e2c-b529-331ffa4c8403">IWMDMOperation3 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 


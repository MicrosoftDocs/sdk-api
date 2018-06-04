---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMPContentPartnerCallback::RefreshLicenseComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>RefreshLicenseComplete</b> method notifies Windows Media Player that the online store has finished processing a request to update the license for a media file.




## -parameters




### -param dwCookie [in]

A cookie that represents a request to update a license for a media file. Windows Media Player previously supplied this cookie to the online store's plug-in by calling <a href="https://msdn.microsoft.com/2f0d8ed9-027c-45a3-a61a-f6d571e78a0a">IWMPContentPartner::RefreshLicense</a>.


### -param contentID [in]

The content ID of the media file for which the license update was requested.


### -param hrRefresh [in]

An <b>HRESULT</b> that indicates whether the license update was successful. Any success code indicates that the update succeeded. Any failure code indicates that the update failed.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Windows Media Player requests a license update by calling the plug-in's <a href="https://msdn.microsoft.com/2f0d8ed9-027c-45a3-a61a-f6d571e78a0a">RefreshLicense</a> method, which initiates the update and returns immediately. When the online store has finished processing the update request, the plug-in calls <b>RefreshLicenseComplete</b>.




## -see-also




<a href="https://msdn.microsoft.com/2f0d8ed9-027c-45a3-a61a-f6d571e78a0a">IWMPContentPartner::RefreshLicense</a>



<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 


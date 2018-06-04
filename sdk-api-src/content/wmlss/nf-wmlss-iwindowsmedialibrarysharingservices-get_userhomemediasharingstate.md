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

# IWindowsMediaLibrarySharingServices::get_userHomeMediaSharingState


## -description


The <b>get_userHomeMediaSharingState</b> method retrieves a value that indicates whether the current user's media library is shared on the home network.


## -parameters




### -param sharingEnabled [out]

Pointer to a <b>VARIANT_BOOL</b> that receives <b>VARIANT_TRUE</b> if the media library is shared and <b>VARIANT_FALSE</b> if the media library is not shared.


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



If home media sharing is not allowed for the computer, this method retrieves <b>VARIANT_FALSE</b> regardless of whether home media sharing is enabled by the current user.

If home media sharing is allowed for the computer and home media sharing is enabled by the current user, this method retrieves <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/9c1ced28-7ed0-4f65-af4d-34774f911621">IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowed</a>



<a href="https://msdn.microsoft.com/d638da61-8196-4d46-ad98-fd7ab8a19e9b">IWindowsMediaLibrarySharingServices::put_userHomeMediaSharingState</a>
 

 


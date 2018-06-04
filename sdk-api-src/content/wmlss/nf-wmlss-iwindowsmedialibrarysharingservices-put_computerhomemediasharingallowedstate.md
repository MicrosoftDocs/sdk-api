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

# IWindowsMediaLibrarySharingServices::put_computerHomeMediaSharingAllowedState


## -description



			The <b>put_computerHomeMediaSharingAllowedState</b> method specifies whether media libraries on the computer are allowed to be shared on the home network.


## -parameters




### -param sharingAllowed

A <b>VARIANT_BOOL</b> that specifies VARIANT_TRUE if media libraries are allowed to be shared  or <b>VARIANT_FALSE</b> if media libraries are not allowed to be shared.


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



This method must be called by code running under elevated privileges.

If home media sharing is not allowed for the computer, none of the users' media libraries are shared on the home network, regardless of whether individual users have enabled home media sharing.


If home media sharing is allowed for the computer and a particular user has enabled media sharing, then that user's media library is shared on the home network.


<div class="alert"><b>Warning</b>  Each call to <b>put_computerHomeMediaSharingAllowedState</b> with the <i>sharingAllowed</i> parameter set to <b>VARIANT_TRUE</b> updates the access control list (ACL) and last changed time  of each file in the computer's Public Music, Public Pictures, and Public Videos folders. This behavior might change in future versions of Windows.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bbec5687-3c77-4385-a9be-74c6d84db962">IWindowsMediaLibrarySharingServices</a>



<a href="https://msdn.microsoft.com/9c1ced28-7ed0-4f65-af4d-34774f911621">IWindowsMediaLibrarySharingServices::get_computerHomeMediaSharingAllowedState</a>
 

 


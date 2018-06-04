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

# ILocationPermissions::CheckLocationCapability


## -description


Gets the location capability of the Windows Store app of the given thread


## -parameters




### -param dwClientThreadId

Thread Id of the app to check the location capability of


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
The method succeeded and the app is location enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The app has not declared location capability or the user has declined or revoked location access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
An invalid client thread was provided.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  <b>CheckLocationCapability</b> is available in Windows 8.</div>
<div> </div>
For more information on location settings in Windows 8 see <a href="https://msdn.microsoft.com/A1FC58B2-D455-4DF7-A4F7-EE0A7E8851DB">Location settings</a>.




## -see-also




<a href="https://msdn.microsoft.com/f4b46f4a-60be-4428-a4b5-6100ae3f1e1b">ILocationPermissions</a>
 

 


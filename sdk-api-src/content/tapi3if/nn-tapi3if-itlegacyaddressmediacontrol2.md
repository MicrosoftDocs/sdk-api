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

# ITLegacyAddressMediaControl2 interface


## -description


The 
<b>ITLegacyAddressMediaControl2</b> interface derives from the 
<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a> interface. 
<b>ITLegacyAddressMediaControl2</b> provides additional methods that allow the configuration of parameters related to line devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLegacyAddressMediaControl2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITLegacyAddressMediaControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLegacyAddressMediaControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac2f7afe-4531-454a-8696-ca21556a049a">ConfigDialog</a>
</td>
<td align="left" width="63%">
Displays a dialog box to allow the user to configure parameters related to the specified line device. The parameters that can be edited are those currently in use on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff3e1cd4-bbd6-43c1-ad55-4787269821da">ConfigDialogEdit</a>
</td>
<td align="left" width="63%">
Displays a dialog box to allow the user to configure parameters related to the specified line device. The parameters to edit are passed in from the application, and the results are returned to the application.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>
 

 


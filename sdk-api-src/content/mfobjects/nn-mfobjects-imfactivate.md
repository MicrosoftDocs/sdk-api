---
UID: NN:mfobjects.IMFActivate
title: IMFActivate
author: windows-sdk-content
description: Enables the application to defer the creation of an object.
old-location: mf\imfactivate.htm
tech.root: medfound
ms.assetid: c0936e3c-3cd1-4c1e-a336-2dee7d943963
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFActivate, IMFActivate interface [Media Foundation], IMFActivate interface [Media Foundation],described, c0936e3c-3cd1-4c1e-a336-2dee7d943963, mf.imfactivate, mfobjects/IMFActivate
ms.topic: interface
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFActivate interface


## -description


Enables the application to defer the creation of an object. This interface is exposed by activation objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFActivate</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFActivate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFActivate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a>
</td>
<td align="left" width="63%">
Creates the object associated with this activation object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15216c57-f85d-4087-ad52-d35059647828">DetachObject</a>
</td>
<td align="left" width="63%">
Detaches the created object from the activation object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f88ff31-5a91-4838-bfce-673a5a85c766">ShutdownObject</a>
</td>
<td align="left" width="63%">
Shuts down the created object.

</td>
</tr>
</table> 


## -remarks



Typically, the application calls some function that returns an <b>IMFActivate</b> pointer and then passes that pointer to another component. The other component calls <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a> at a later time to create the object. In the protected media path (PMP), the <b>IMFActivate</b> pointer might be marshaled to the protected process, so that the object can be created in that process.




## -see-also




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


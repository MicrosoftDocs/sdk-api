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

# IWMPContentPartner::Login


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>Login</b> method logs the user in to the online store.




## -parameters




### -param userInfo [in]

Encrypted <b>BLOB</b> containing the user name.


### -param pwdInfo [in]

Encrypted <b>BLOB</b> containing the user password.


### -param fUsedCachedCreds [in]

<b>VARIANT_BOOL</b> indicating whether the plug-in should try to use cached credentials.


### -param fOkToCache [in]

<b>VARIANT_BOOL</b> indicating whether the plug-in is permitted to cache the supplied credentials.


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



Usually, this method is called in response to a specific request by the user to log in to the online store. Sometimes, the need to log in is implied by other user actions, such as burning a music file that requires an updated license.

The plug-in must call <a href="https://msdn.microsoft.com/e8402662-7e14-4be7-bc2d-45338bf2a226">IWMPContentPartnerCallback::Notify</a> to notify Windows Media Player when the log-in state changes.

To decrypt the user name and password, use the <b>CryptUnprotectData</b> function. <b>CryptUnprotectData</b> is documented in the Cryptography section of the Platform SDK. You must use the CRYPTPROTECT_UI_FORBIDDEN flag in the <i>dwFlags</i> parameter of <b>CryptUnprotectData</b>. Set the optional and reserved parameters to <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/8919dd66-1ec0-4551-8132-7067957bb545">IWMPContentPartner::Logout</a>
 

 


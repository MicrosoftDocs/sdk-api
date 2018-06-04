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

# IWMPContentPartnerCallback::VerifyPermissionComplete


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>VerifyPermissionComplete</b> method notifies Windows Media Player that the online store has finished processing a call to <a href="https://msdn.microsoft.com/7ff45264-6e49-4953-bc0a-b3652aee965d">IWMPContentPartner::VerifyPermission</a>.




## -parameters




### -param bstrPermission [in]

A <b>BSTR</b> that specifies the action for which permission was requested. Windows Media Player previously requested permission to perform this action by calling <a href="https://msdn.microsoft.com/7ff45264-6e49-4953-bc0a-b3652aee965d">IWMPContentPartner::VerifyPermission</a>. See Remarks for a list of possible values.


### -param pContext [in]

A pointer to a <b>VARIANT</b> that contains information related to the notification. See Remarks.


### -param hrPermission [in]

An <b>HRESULT</b> that indicates whether permission is granted. Any success code indicates that permission is granted. Any failure code indicates that permission is denied.


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



The following list gives the possible values for <i>bstrPermission</i> and the corresponding meanings of <i>pContext</i>.

g_szVerifyPermissionSync

Windows Media Player previously requested permission to synchronize the content on a portable device by calling <b>IWMPContentPartner::VerifyPermission</b>. In that call, Windows Media Player supplied the canonical device name in the <i>pContext</i> parameter. The online store supplies that same canonical device name in the <i>pContext</i> parameter of <b>VerifyPermissionComplete</b>.




## -see-also




<a href="https://msdn.microsoft.com/7ff45264-6e49-4953-bc0a-b3652aee965d">IWMPContentPartner::VerifyPermission</a>



<a href="https://msdn.microsoft.com/3c66052b-2b82-44aa-868d-5d5a4501c457">IWMPContentPartnerCallback Interface</a>
 

 


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

# IWMPContentPartner::VerifyPermission


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>VerifyPermission</b> method initiates the process of verifying permission for Windows Media Player to perform an action.




## -parameters




### -param bstrPermission [in]

A <b>BSTR</b> that specifies the action for which permission is being requested. See Remarks for a list of possible values.


### -param pContext [in]

A pointer to a <b>VARIANT</b> that contains information related to the request. See Remarks.


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



The <b>VerifyPermission</b> method initiates a permission verification and then returns immediately. When the online store has completed the verification, it calls <a href="https://msdn.microsoft.com/bf99ead7-a50c-4638-9f4c-5c43a8d0a0be">IWMPContentPartnerCallback::VerifyPermissionComplete</a> to notify Windows Media Player that permission has been granted or denied.

The following list gives the possible values for <i>bstrPermission</i> along with the corresponding meanings of <i>pContext</i>.

g_szVerifyPermissionSync

Windows Media Player is requesting permission from the online store to synchronize the content on a portable device. The <i>pContext</i> parameter is a <b>VT_BSTR</b> that specifies the canonical device name.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/bf99ead7-a50c-4638-9f4c-5c43a8d0a0be">IWMPContentPartnerCallback::VerifyPermissionComplete</a>
 

 


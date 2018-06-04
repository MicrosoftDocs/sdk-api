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

# PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN callback function


## -description


Called by the Windows Biometric Framework to set the extended default and per-user antispoofing policies used by the engine adapter.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param PolicyItemArray [in]

Address of an array of <a href="https://msdn.microsoft.com/7098FC53-E487-42B2-8B4B-EB7E2D296CB6">WINBIO_ACCOUNT_POLICY</a> structures, which the routine should use to update the policies it is applying to any identities it detects.


### -param PolicyItemCount [in]

The number of elements in the array pointed to by the <i>PolicyItemArray</i> parameter.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_some_error </b></dt>
</dl>
</td>
<td width="60%">
Errors return by the method are logged but ignored.

</td>
</tr>
</table>
 




## -remarks



This method is called each time the biometric unit is activated.

This method executes in the context of the same thread that activated the biometric unit and that processed all other requests for the unit.

The Identity.Type field of the first element in the <i>PolicyItemArray</i> will always be <b>WINBIO_ID_TYPE_WILDCARD</b>. This indicates that the policy item contains a default AntiSpoofBehavior value which should be applied to any user account that isn’t explicitly listed in the rest of the array.

If the <i>PolicyItemArray</i> contains more than one element, the Identity.Type field of the remaining items will be <b>WINBIO_ID_TYPE_WILDCARD</b>, and the Identity.Value.AccountSid.Data field will contain the SID of a user account that requires the antispoof policy behavior specified in the AntiSpoofBehavior field of the array element.




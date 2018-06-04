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

# IAzClientContext3::GetGroups


## -description


The <b>GetGroups</b> method returns an array of the application groups associated with this client context.


## -parameters




### -param bstrScopeName [in]

The name of the scope in which to check for application groups. This parameter is ignored if the value of the ulOptions parameter is set to <b>AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY</b>.


### -param ulOptions [in]

A set of flags that modify the behavior of this method. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY"></a><a id="az_client_context_get_groups_store_level_only"></a><dl>
<dt><b>AZ_CLIENT_CONTEXT_GET_GROUPS_STORE_LEVEL_ONLY</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
This method checks only for application groups at the store level.

</td>
</tr>
</table>
 


### -param pGroupArray [out]

A pointer to an array of the names of application groups associated with this client context.

This is a variant that contains either a <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> or the  JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains the name of an application group.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/9435e41b-b2ec-4a2a-9058-82025f2c2e09">IAzClientContext3</a>
 

 


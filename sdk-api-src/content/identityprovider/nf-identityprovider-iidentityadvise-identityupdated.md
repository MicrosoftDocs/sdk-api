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

# IIdentityAdvise::IdentityUpdated


## -description


The <b>IdentityUpdated</b> method is called by an identity provider to notify a calling application that an identity event occurred. An application calls the <a href="https://msdn.microsoft.com/fcac9d30-64ed-4746-aacc-ee659c2b2642">IIdentityProvider::Advise</a> method to specify events for which it is to be notified.


## -parameters




### -param dwIdentityUpdateEvents [in]

The identity events that occurred. The value of this parameter can be zero or more of the following values combined by using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_ASSOCIATED"></a><a id="identity_associated"></a><dl>
<dt><b>IDENTITY_ASSOCIATED</b></dt>
<dt>0X0001</dt>
</dl>
</td>
<td width="60%">
An identity was associated with the identity provider.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_DISASSOCIATED"></a><a id="identity_disassociated"></a><dl>
<dt><b>IDENTITY_DISASSOCIATED</b></dt>
<dt>0X0002</dt>
</dl>
</td>
<td width="60%">
An identity was disassociated from the identity provider.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_CREATED"></a><a id="identity_created"></a><dl>
<dt><b>IDENTITY_CREATED</b></dt>
<dt>0X0004</dt>
</dl>
</td>
<td width="60%">
A new identity was created.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_IMPORTED"></a><a id="identity_imported"></a><dl>
<dt><b>IDENTITY_IMPORTED</b></dt>
<dt>0X0008</dt>
</dl>
</td>
<td width="60%">
An identity was imported from another identity provider.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_DELETED"></a><a id="identity_deleted"></a><dl>
<dt><b>IDENTITY_DELETED</b></dt>
<dt>0X0010</dt>
</dl>
</td>
<td width="60%">
An identity was deleted from the identity store.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_PROPCHANGE"></a><a id="identity_propchange"></a><dl>
<dt><b>IDENTITY_PROPCHANGE</b></dt>
<dt>0X0020</dt>
</dl>
</td>
<td width="60%">
The value of  a property of an identity changed.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_CONNECTED"></a><a id="identity_connected"></a><dl>
<dt><b>IDENTITY_CONNECTED</b></dt>
<dt>0X0040</dt>
</dl>
</td>
<td width="60%">
The identity is a connected identity.

</td>
</tr>
<tr>
<td width="40%"><a id="IDENTITY_DISCONNECTED"></a><a id="identity_disconnected"></a><dl>
<dt><b>IDENTITY_DISCONNECTED</b></dt>
<dt>0X0080</dt>
</dl>
</td>
<td width="60%">
The identity was disconnected from the identity provider.

</td>
</tr>
</table>
 


### -param lpszUniqueID [in]

The identity associated with the events that occurred.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/fa348d46-bcd2-4009-89d6-11e738d4a82b">IIdentityAdvise</a>
 

 


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

# _TOKEN_MANDATORY_POLICY structure


## -description


The <b>TOKEN_MANDATORY_POLICY</b> structure specifies the mandatory integrity policy for a token.


## -struct-fields




### -field Policy

The mandatory integrity access policy for the associated token. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TOKEN_MANDATORY_POLICY_OFF"></a><a id="token_mandatory_policy_off"></a><dl>
<dt><b>TOKEN_MANDATORY_POLICY_OFF</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
No mandatory integrity policy is enforced for the token.

</td>
</tr>
<tr>
<td width="40%"><a id="TOKEN_MANDATORY_POLICY_NO_WRITE_UP"></a><a id="token_mandatory_policy_no_write_up"></a><dl>
<dt><b>TOKEN_MANDATORY_POLICY_NO_WRITE_UP</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
A process associated with the token cannot write to objects that have a greater mandatory integrity level.

</td>
</tr>
<tr>
<td width="40%"><a id="TOKEN_MANDATORY_POLICY_NEW_PROCESS_MIN"></a><a id="token_mandatory_policy_new_process_min"></a><dl>
<dt><b>TOKEN_MANDATORY_POLICY_NEW_PROCESS_MIN</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
A process created with the token has an integrity level that is the lesser of the parent-process integrity level and the executable-file integrity level.

</td>
</tr>
<tr>
<td width="40%"><a id="TOKEN_MANDATORY_POLICY_VALID_MASK"></a><a id="token_mandatory_policy_valid_mask"></a><dl>
<dt><b>TOKEN_MANDATORY_POLICY_VALID_MASK</b></dt>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
A combination of <b>TOKEN_MANDATORY_POLICY_NO_WRITE_UP</b> and <b>TOKEN_MANDATORY_POLICY_NEW_PROCESS_MIN</b>.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556838">TOKEN_INFORMATION_CLASS</a>
 

 


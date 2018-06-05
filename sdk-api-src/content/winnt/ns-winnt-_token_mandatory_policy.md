---
UID: NS:winnt._TOKEN_MANDATORY_POLICY
title: "_TOKEN_MANDATORY_POLICY"
author: windows-sdk-content
description: Specifies the mandatory integrity policy for a token.
old-location: security\token_mandatory_policy.htm
old-project: SecAuthZ
ms.assetid: f5fc438b-c4f0-46f6-a188-52ce660d13da
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PTOKEN_MANDATORY_POLICY, PTOKEN_MANDATORY_POLICY, PTOKEN_MANDATORY_POLICY structure pointer [Security], TOKEN_MANDATORY_POLICY, TOKEN_MANDATORY_POLICY structure [Security], TOKEN_MANDATORY_POLICY_NEW_PROCESS_MIN, TOKEN_MANDATORY_POLICY_NO_WRITE_UP, TOKEN_MANDATORY_POLICY_OFF, TOKEN_MANDATORY_POLICY_VALID_MASK, _TOKEN_MANDATORY_POLICY, security.token_mandatory_policy, winnt/PTOKEN_MANDATORY_POLICY, winnt/TOKEN_MANDATORY_POLICY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TOKEN_MANDATORY_POLICY, *PTOKEN_MANDATORY_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	TOKEN_MANDATORY_POLICY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 


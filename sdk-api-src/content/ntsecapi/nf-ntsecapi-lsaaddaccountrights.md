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

# LsaAddAccountRights function


## -description


The <b>LsaAddAccountRights</b> function assigns one or more <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> to an account. If the account does not exist, <b>LsaAddAccountRights</b> creates it.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle must have the POLICY_LOOKUP_NAMES access right. If the account identified by the <i>AccountSid</i> parameter does not exist, the handle must have the POLICY_CREATE_ACCOUNT access right. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param AccountSid [in]

Pointer to the SID of the account to which the function assigns <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a>.


### -param UserRights [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structures. Each structure contains the name of a privilege to add to the account. For a list of privilege names, see 
<a href="https://msdn.microsoft.com/be5637e3-0932-49b6-a5af-a542060545e0">Privilege Constants</a>.


### -param CountOfRights [in]

Specifies the number of elements in the <i>UserRights</i> array.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_PRIVILEGE</b></dt>
</dl>
</td>
<td width="60%">
One of the privilege names is not valid.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -remarks



If you specify privileges already granted to the account, they are ignored.

For an example that demonstrates calling this function, see 
<a href="https://msdn.microsoft.com/c28c03f0-4638-42ed-8dad-1e934cf99273">Managing Account Permissions</a>.




## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/3f4a4a9a-66ca-410a-8bdc-c390e8b966e3">LsaEnumerateAccountRights</a>



<a href="https://msdn.microsoft.com/ad250a01-7a24-4fae-975c-aa3e65731c82">LsaRemoveAccountRights</a>
 

 


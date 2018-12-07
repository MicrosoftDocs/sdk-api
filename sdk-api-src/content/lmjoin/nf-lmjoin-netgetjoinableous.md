---
UID: NF:lmjoin.NetGetJoinableOUs
title: NetGetJoinableOUs function
author: windows-sdk-content
description: The NetGetJoinableOUs function retrieves a list of organizational units (OUs) in which a computer account can be created.
old-location: netmgmt\netgetjoinableous.htm
tech.root: netmgmt
ms.assetid: 1faa912b-c56d-431c-95d5-d36790b0d467
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NetGetJoinableOUs, NetGetJoinableOUs function [Network Management], _win32_netgetjoinableous, lmjoin/NetGetJoinableOUs, netmgmt.netgetjoinableous
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmjoin.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetGetJoinableOUs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetGetJoinableOUs function


## -description


The
				<b>NetGetJoinableOUs</b> function retrieves a list of organizational units (OUs) in which a computer account can be created.


## -parameters




### -param lpServer [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the computer on which to call the function. If this parameter is <b>NULL</b>, the local computer is used.


### -param lpDomain [in]

Pointer to a constant string that specifies the name of the domain for which to retrieve the list of OUs that can be joined.


### -param lpAccount [in]

Pointer to a constant string that specifies the account name to use when connecting to the domain controller. The string must specify either a domain NetBIOS name and user account (for example, "REDMOND\user") or the user principal name (UPN) of the user in the form of an Internet-style login name (for example, "someone@example.com"). If this parameter is <b>NULL</b>, the caller's context is used.


### -param lpPassword [in]

If the <i>lpAccount</i> parameter specifies an account name, this parameter must point to the password to use when connecting to the domain controller. Otherwise, this parameter must be <b>NULL</b>.


### -param OUCount [out]

Receives the count of OUs returned in the list of joinable OUs.


### -param OUs [out]

Pointer to an array that receives the list of joinable OUs. This array is allocated by the system and must be freed using a single call to the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes or one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_DefaultJoinRequired</b></dt>
</dl>
</td>
<td width="60%">
The destination domain controller does not support creating computer accounts in OUs.

</td>
</tr>
</table>
 




## -remarks



No special group membership is required to successfully execute the 
<b>NetGetJoinableOUs</b> function.

For more information about organizational units, see 
<a href="https://msdn.microsoft.com/57c83e4d-2d9f-4f22-97e2-27e2d277f014">Managing Users</a> in the Active Directory documentation.




## -see-also




<a href="https://msdn.microsoft.com/c7cc1cf2-4530-4039-806b-fbee572f564d">NetGetJoinInformation</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 


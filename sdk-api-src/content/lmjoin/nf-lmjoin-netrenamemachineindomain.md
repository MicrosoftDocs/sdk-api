---
UID: NF:lmjoin.NetRenameMachineInDomain
title: NetRenameMachineInDomain function
author: windows-sdk-content
description: The NetRenameMachineInDomain function changes the name of a computer in a domain.
old-location: netmgmt\netrenamemachineindomain.htm
tech.root: netmgmt
ms.assetid: 1f7ddaa1-a349-49a6-856d-a2fde2f1dc3b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: NetRenameMachineInDomain, NetRenameMachineInDomain function [Network Management], _win32_netrenamemachineindomain, lmjoin/NetRenameMachineInDomain, netmgmt.netrenamemachineindomain
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
 - NetRenameMachineInDomain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetRenameMachineInDomain function


## -description


The 
				<b>NetRenameMachineInDomain</b> function changes the name of a computer in a domain.


## -parameters




### -param lpServer [in]

A pointer to a constant string that specifies the DNS or NetBIOS name of the computer on which to call the function. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param lpNewMachineName [in]

A pointer to a constant string that specifies the new name of the computer. If specified, the local computer name is changed as well. If this parameter is <b>NULL</b>, the function assumes you have already called the 
<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a> function.


### -param lpAccount [in]

A pointer to a constant string that specifies an account name to use when connecting to the domain controller. If this parameter is <b>NULL</b>, the caller's context is used.


### -param lpPassword [in]

If the <i>lpAccount</i> parameter specifies an account name, this parameter must point to the password to use when connecting to the domain controller. Otherwise, this parameter must be <b>NULL</b>.


### -param fRenameOptions [in]

The rename options. If this parameter is NETSETUP_ACCT_CREATE, the function renames the account in the domain.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned if the account name passed in the <i>lpAccount</i> parameter did not have sufficient access rights for the operation. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_SetupNotJoined</b></dt>
</dl>
</td>
<td width="60%">
The computer is not currently joined to a domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_SetupDomainController</b></dt>
</dl>
</td>
<td width="60%">
This computer is a domain controller and cannot be unjoined from a domain.

</td>
</tr>
</table>
 




## -remarks



Renaming a domain computer can be performed only by a user that is a member of the Administrators local group on the target computer and that also is a member of the Administrators group on the domain or has the Account Operator privilege on the domain. If you call the 
<b>NetRenameMachineInDomain</b> function remotely, you must supply credentials because you cannot delegate credentials under these circumstances.

Different processes, or different threads of the same process, should not call the 
<b>NetRenameMachineInDomain</b> function at the same time. This situation can leave the computer in an inconsistent state.

The <b>NERR_SetupNotJoined</b> and  <b>NERR_SetupDomainController</b> return values are defined in the Lmerr.h header file. This header file is automatically included by the Lm.h header file and should not be included directly.

A system reboot is required after calling the <b>NetRenameMachineInDomain</b> function for the operation to complete.




## -see-also




<a href="https://msdn.microsoft.com/710865c6-e327-439c-931d-de8674d69233">NetAddAlternateComputerName</a>



<a href="https://msdn.microsoft.com/c657ae33-404e-4c36-a956-5fbcfa540be7">NetEnumerateComputerNames</a>



<a href="https://msdn.microsoft.com/3c7ab44e-d5fa-40da-83fe-a44bf85b2ba5">NetRemoveAlternateComputerName</a>



<a href="https://msdn.microsoft.com/524c8219-a303-45ab-95e2-91319b477568">NetSetPrimaryComputerName</a>



<a href="https://msdn.microsoft.com/cc755c22-1fd6-4787-999e-a43258287a05">NetUnjoinDomain</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a>
 

 


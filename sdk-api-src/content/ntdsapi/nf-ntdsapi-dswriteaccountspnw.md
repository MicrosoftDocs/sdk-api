---
UID: NF:ntdsapi.DsWriteAccountSpnW
title: DsWriteAccountSpnW function
author: windows-sdk-content
description: Writes an array of service principal names (SPNs) to the servicePrincipalName attribute of a specified user or computer account object in Active Directory Domain Services.
old-location: ad\dswriteaccountspn.htm
tech.root: AD
ms.assetid: 2b555f6b-643d-4fa0-9aca-701e6b3313fa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DsWriteAccountSpn, DsWriteAccountSpn function [Active Directory], DsWriteAccountSpnA, DsWriteAccountSpnW, _glines_dswriteaccountspn, ad.dswriteaccountspn, ntdsapi/DsWriteAccountSpn, ntdsapi/DsWriteAccountSpnA, ntdsapi/DsWriteAccountSpnW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsWriteAccountSpnW (Unicode) and DsWriteAccountSpnA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsWriteAccountSpn
 - DsWriteAccountSpnA
 - DsWriteAccountSpnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DsWriteAccountSpnW function


## -description


The <b>DsWriteAccountSpn</b> function writes an array of service principal names (SPNs) to the <b>servicePrincipalName</b> attribute of a specified user or computer account object in Active Directory Domain Services. The function can either register or unregister the SPNs.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param Operation [in]

Contains one of the <a href="https://msdn.microsoft.com/8367bdaf-3d8d-46b3-9d03-b9753e8e5a1a">DS_SPN_WRITE_OP</a> values that specifies the operation that <b>DsWriteAccountSpn</b> will perform.


### -param pszAccount [in]

Pointer to a constant null-terminated string that specifies the distinguished name of a user or computer object in Active Directory Domain Services. The caller must have write access to the <b>servicePrincipalName</b> property of this object.


### -param cSpn [in]

Specifies the number of SPNs in <i>rpszSpn</i>. If this value is zero, and <i>Operation</i> contains <b>DS_SPN_REPLACE_SPN_OP</b>, the function removes all values from the <b>servicePrincipalName</b> attribute of the specified account.


### -param rpszSpn [in]

Pointer to an array of constant null-terminated strings that specify the SPNs to be added to or removed from the  account identified by the <i>pszAccount</i> parameter. The <a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSpn</a> function is used to compose SPNs for a service.


## -returns



Returns <b>ERROR_SUCCESS</b> if successful or a Win32, RPC or directory service error if unsuccessful.




## -remarks



The <b>DsWriteAccountSpn</b> function registers the SPNs for one or more instances of a service. SPNs are used by clients, in conjunction with a trusted authentication service, to authenticate the service. To protect against security attacks where an application or service fraudulently registers an SPN that identifies some other service, the default DACL on user and computer accounts allows only domain administrators to register SPNs in most cases.

One exception to this rule is that a service running under the LocalSystem account can call <b>DsWriteAccountSpn</b> to register a simple SPN of the form "ServiceClass/Host:Port" if the host specified in the SPN is the DNS or NetBIOS name of the computer on which the service is running.

Another exception is that the default DACL on computer accounts allows callers to register SPNs on themselves, subject to certain constraints.  For example, a computer account can have SPNs relative to its computername, of the form "host/&lt;computername&gt;".  Because the computername is contained in the SPN, the SPN is allowable.

None of the rules above apply if the DSA is configured to allow any SPN to be written. This reduces security, however, so it is not recommended.

SPNs passed to <b>DsWriteAccountSpn</b> are actually added to the <b>Service-Principal-Name</b> attribute of the computer object in <i>pszAccount</i>. This call is made using RPC to the domain controller where the account object is stored so it can securely enforce policy on what SPNs are allowed on the account. Using LDAP to write directly to the SPN property is not allowed; all writes must come through this RPC call. Reads using LDAP are allowed.

Permissions required to set SPNs

To write an arbitrary SPN on an account, the writer requires the "Write ServicePrincipalName"  right, which is not granted by default  to the person who created the account. That person  has the 'Write validated SPN" right(present only on machine accounts).

Below is a summary of rights per user on machine accounts:

<table>
<tr>
<th>User Type</th>
<th>Rights</th>
</tr>
<tr>
<td>Person creating the Account</td>
<td>Write validated SPN</td>
</tr>
<tr>
<td>Account Operators</td>
<td>Write SPN and Write Validated SPN</td>
</tr>
<tr>
<td>Authenticated Users</td>
<td>None</td>
</tr>
<tr>
<td>(self)</td>
<td>Write Validated SPN</td>
</tr>
</table>
 

On user accounts there is no "Validated SPN" property or "Write SPN" right.  Rather, the  "Write public information" property set grants the ability to create arbitrary SPNs.




## -see-also




<a href="https://msdn.microsoft.com/8367bdaf-3d8d-46b3-9d03-b9753e8e5a1a">DS_SPN_WRITE_OP</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/cbd53850-9b05-4f74-ab07-30dcad583fc5">DsGetSpn</a>
 

 


---
UID: NF:ntdsapi.DsServerRegisterSpnW
title: DsServerRegisterSpnW function (ntdsapi.h)
description: The DsServerRegisterSpn function composes two SPNs for a host-based service. (Unicode)
helpviewer_keywords: ["DS_SPN_ADD_SPN_OP", "DS_SPN_DELETE_SPN_OP", "DS_SPN_REPLACE_SPN_OP", "DsServerRegisterSpn", "DsServerRegisterSpn function [Active Directory]", "DsServerRegisterSpnW", "_glines_dsserverregisterspn", "ad.dsserverregisterspn", "ntdsapi/DsServerRegisterSpn", "ntdsapi/DsServerRegisterSpnW"]
old-location: ad\dsserverregisterspn.htm
tech.root: ad
ms.assetid: d95dfa55-f978-4d8d-a63d-cd1339769c79
ms.date: 12/05/2018
ms.keywords: DS_SPN_ADD_SPN_OP, DS_SPN_DELETE_SPN_OP, DS_SPN_REPLACE_SPN_OP, DsServerRegisterSpn, DsServerRegisterSpn function [Active Directory], DsServerRegisterSpnA, DsServerRegisterSpnW, _glines_dsserverregisterspn, ad.dsserverregisterspn, ntdsapi/DsServerRegisterSpn, ntdsapi/DsServerRegisterSpnA, ntdsapi/DsServerRegisterSpnW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsServerRegisterSpnW (Unicode) and DsServerRegisterSpnA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsServerRegisterSpnW
 - ntdsapi/DsServerRegisterSpnW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsServerRegisterSpn
 - DsServerRegisterSpnA
 - DsServerRegisterSpnW
---

# DsServerRegisterSpnW function


## -description

The <b>DsServerRegisterSpn</b> function composes two SPNs for a host-based service. The names are based on the DNS and NetBIOS names of the local computer. The function modifies the <b>servicePrincipalName</b> attribute of either a specified account or of the account associated with the calling thread. The function either registers or unregisters the SPNs.

A host-based service is a service instance that provides services identified with its host computer, as distinguished from a replicable service where clients have no preference which host computer a service instance runs on.

## -parameters

### -param Operation [in]

Specifies what operation <b>DsServerRegisterSpn</b> should perform. This parameter can have one of the following values.



#### DS_SPN_ADD_SPN_OP

Adds the SPNs to the user or computer account.



#### DS_SPN_DELETE_SPN_OP

Deletes the specified SPNs from the account.



#### DS_SPN_REPLACE_SPN_OP

Removes all SPNs currently registered on the user or computer account and replaces them with the new SPNs.

### -param ServiceClass [in]

Pointer to a constant null-terminated string specifying the class of the service. This parameter may be any string unique to that service; either the protocol name (for example, ldap) or the string form of a GUID will work.

### -param UserObjectDN [in, optional]

Pointer to a constant null-terminated string specifying the distinguished name of a user or computer account object to write the SPNs to. If this parameter is <b>NULL</b>, <b>DsServerRegisterSpn</b> writes to the account object of the primary or impersonated user associated with the calling thread. If the thread is running in the security context of the LocalSystem account, the function writes to the account object of the local computer.


##### - Operation.DS_SPN_ADD_SPN_OP

Adds the SPNs to the user or computer account.


##### - Operation.DS_SPN_DELETE_SPN_OP

Deletes the specified SPNs from the account.


##### - Operation.DS_SPN_REPLACE_SPN_OP

Removes all SPNs currently registered on the user or computer account and replaces them with the new SPNs.

## -returns

If the function successfully registers one or more SPNs, it returns <b>ERROR_SUCCESS</b>. Modification is performed permissively, so that adding a value that already exists does not return an error.

## -remarks

The two SPNs composed by the <b>DsServerRegisterSpn</b> function have the following format:


```cpp
<ServiceClass>/<host>
```


In one SPN, the host computer is the fully qualified DNS name of the local computer. In the other SPN, the host component is the NetBIOS name of the local computer.

In most cases, the <b>DsServerRegisterSpn</b> caller must have domain administrator privileges to successfully modify the <b>servicePrincipalName</b> attribute of an account object. The exception to this rule is if the calling thread is running under the LocalSystem account, <b>DsServerRegisterSpn</b> is allowed if the <i>UserObjectDN</i> parameter is either <b>NULL</b> or specifies the distinguished name of the local computer account.





> [!NOTE]
> The ntdsapi.h header defines DsServerRegisterSpn as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetspna">DsGetSpn</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dswriteaccountspna">DsWriteAccountSpn</a>

---
UID: NS:winldap.LdapReferralCallback
title: LdapReferralCallback
author: windows-sdk-content
description: Used to implement external caching of connections.
old-location: ldap\ldap_referral_callback.htm
tech.root: ldap
ms.assetid: e5fe6a4b-00e7-4837-b1c1-8b2a724bb75e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PLDAP_REFERRAL_CALLBACK, LDAP_REFERRAL_CALLBACK, LDAP_REFERRAL_CALLBACK structure [LDAP], LdapReferralCallback, PLDAP_REFERRAL_CALLBACK, PLDAP_REFERRAL_CALLBACK structure pointer [LDAP], _ldap_ldap_referral_callback, ldap.ldap__referral__callback, ldap.ldap_referral_callback, winldap/LDAP_REFERRAL_CALLBACK, winldap/PLDAP_REFERRAL_CALLBACK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAP_REFERRAL_CALLBACK
product: Windows
targetos: Windows
req.typenames: LDAP_REFERRAL_CALLBACK, *PLDAP_REFERRAL_CALLBACK
req.redist: 
---

# LdapReferralCallback structure


## -description


The <b>LDAP_REFERRAL_CALLBACK</b> structure is used to implement external caching of connections. This structure is used only when tracking referrals.


## -struct-fields




### -field SizeOfCallbacks

The amount of memory required for the callback. Set this field to <code>sizeof(LDAP_REFERRAL_CALLBACK)</code>.


### -field QueryForConnection

A pointer to a callback function to determine whether there is a cached connection cached available. For more information, see Remarks.


### -field NotifyRoutine

A pointer to a callback function that determines whether a new connection will be cached or destroyed after the operation completes. For more information, see Remarks.


### -field DereferenceRoutine

A pointer to a callback function to dereference a connection that is not in use. For more information, see Remarks.


## -remarks



Use the <b>LDAP_REFERRAL_CALLBACK</b> structure to implement a mechanism for caching connections. The structure contains three callback functions which you implement in your client code.

<b>QUERYFORCONNECTION</b>: If a connection is available, this function should return a pointer to the connection to use in <i>ConnectionToUse</i>. If no connection is available, the function should set <i>ConnectionToUse</i> to <b>NULL</b>. The signature for this callback function is as follows.


```cpp
typedef ULONG (_cdecl QUERYFORCONNECTION)(
    PLDAP       PrimaryConnection,
    PLDAP       ReferralFromConnection,
    PWCHAR      NewDN,
    PCHAR       HostName,
    ULONG       PortNumber,
    PVOID       SecAuthIdentity,    // If NULL, use CurrentUser below
    PVOID       CurrentUserToken,   // pointer to current user LUID.
    PLDAP       *ConnectionToUse
);
```


<b>NOTIFYOFNEWCONNECTION</b>: The run time calls this function if a new connection was created in the course of chasing a referral. This function should return <b>FALSE</b> if not required to cache the connection. When <b>FALSE</b> is returned, the connection is destroyed when the operation completes. The function should return <b>TRUE</b> if it has taken ownership of the connection and the connection will be cached. Be aware that any new connections so created inherit the current callbacks from the primary connection on which the request was initiated. The signature for this function is.


```cpp
typedef BOOLEAN (_cdecl NOTIFYOFNEWCONNECTION) 
    (
    PLDAP       PrimaryConnection,
    PLDAP       ReferralFromConnection,
    PWCHAR      NewDN,
    PCHAR       HostName,
    PLDAP       NewConnection,
    ULONG       PortNumber,
    PVOID       SecAuthIdentity,    // If null, use CurrentUser below.
    PVOID       CurrentUser,        // Pointer to current user LUID.
    ULONG       ErrorCodeFromBind   // If nonzero, bind to server failed.
    );
```


<b>DEREFERENCECONNECTION</b>: The LDAP run time calls this function to dereference a connection that is no longer required. The connection may have come from a successful call to <b>QueryForConnection</b> or from <b>NotifyOfNewConnection</b>. The function should return LDAP_SUCCESS if the call succeeds; currently, however, the run time ignores the return value. The signature for this function is as follows.


```cpp
typedef ULONG (_cdecl DEREFERENCECONNECTION)
    (
    PLDAP       PrimaryConnection,
    PLDAP       ConnectionToDereference
    );
```


To configure a session to use callbacks to obtain a cached connection, call 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a> (conn, LDAP_OPT_REFERRAL_CALLBACK, &amp;referralRoutines), where <i>referralRoutines</i> is the address of the <b>LDAP_REFERRAL_CALLBACK</b> structure that contains your routines. The addresses may be <b>NULL</b>, in which case the LDAP run time will not make the calls.

The parameter descriptions for the preceding three functions are as follows:

<ul>
<li>
<i>PrimaryConnection</i>

The LDAP connection handle on which the operation was originally performed. For example, the handle passed in to a call to <a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a>, <a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>, <a href="https://msdn.microsoft.com/d978f668-7726-44e4-a0b1-31390e8498c4">ldap_add</a>, and so on.

</li>
<li>
<i>ReferralFromConnection</i>

The connection which sent the referral currently tracked. Referrals can be tracked across multiple "hops". For example, the referral can be from the original server to a second server, then the second server can refer the operation to a third server, and so on. If <i>ReferralFromConnection</i> equates to <i>PrimaryConnection</i>, the first "hop" is being tracked (a referral sent from the original server).

</li>
<li>
<i>NewDN</i>

Pointer to a wide, null-terminated string that contains the DN of the referred-to object.

</li>
<li>
<i>HostName</i>

Pointer to a null-terminated string that contains the name of the referred-to server; that is the server to which a connection must be made.

</li>
<li><i>PortNumber</i>Port on the referred-to server, to which a connection must be made.

</li>
<li>
<i>SecAuthIdentity</i>

The <b>SEC_WINNT_AUTH_IDENTITY</b> or <b>SEC_WINNT_AUTH_IDENTITY_EX</b> for the credentials used when tracking the referral, or a <b>NULL</b> if the user's default credentials are used.

</li>
<li>
<i>CurrentUserToken/CurrentUser</i>

The AuthenticationID LUID of the user for which a connection is required. If <i>SecAuthIdentity</i> is <b>NULL</b>, use this parameter to identify the user.

</li>
<li>
<i>NewConnection</i>

Used to announce the existence of the  new connection.

</li>
<li>
<i>ErrorCodeFromBind</i>

Error code returned from <a href="https://msdn.microsoft.com/67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4">ldap_bind_s</a> when an attempt is made to  bind to the newly created connection (<i>NewConnection</i>).

</li>
<li>
<i>ConnectionToDereference</i>

The connection to be dereferenced.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>



<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>
 

 


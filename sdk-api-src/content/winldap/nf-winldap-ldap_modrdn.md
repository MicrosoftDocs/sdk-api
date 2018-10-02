---
UID: NF:winldap.ldap_modrdn
title: ldap_modrdn function
author: windows-sdk-content
description: The ldap_modrdn function changes the relative distinguished name of an LDAP entry.
old-location: ldap\ldap_modrdn.htm
tech.root: LDAP
ms.assetid: 7a85eb4d-dcb1-4a5b-a7df-1d726215bde3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "_ldap_ldap_modrdn, ldap.ldap__modrdn, ldap.ldap_modrdn, ldap_modrdn, ldap_modrdn function [LDAP], ldap_modrdnA, ldap_modrdnW, winldap/ldap_modrdn, winldap/ldap_modrdnA, winldap/ldap_modrdnW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modrdnW (Unicode) and ldap_modrdnA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_modrdn
 - ldap_modrdnA
 - ldap_modrdnW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_modrdn function


## -description


The <b>ldap_modrdn</b> function changes the relative distinguished name of an LDAP entry.

This function is obsolete and is provided for backward compatibility with earlier versions of LDAP. For LDAP 3 or later, use the 
<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a> or 
<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a> functions.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param DistinguishedName [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to be changed.


### -param NewDistinguishedName [out]

A pointer to a null-terminated string that contains the new relative distinguished name to give the entry.


## -returns



If the function succeeds, it returns the message ID of the modify operation.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.




## -remarks



Use the <b>ldap_modrdn</b> function, or its synchronous equivalent, 
<a href="https://msdn.microsoft.com/0ea0c52d-5056-4ccf-bc64-87a2f0ebd0c5">ldap_modrdn_s</a>, to change the name of an LDAP entry. LDAP 2 supports additional features through 
<a href="https://msdn.microsoft.com/7bf7370f-a5e6-474e-8fe9-e6895ef48ab5">ldap_modrdn2</a> and 
<a href="https://msdn.microsoft.com/a2cf121d-4e84-4195-9080-3b6c0c4cea82">ldap_modrdn2_s</a>.

As an asynchronous function, <b>ldap_modrdn</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous add operation before it has completed, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

Be aware that the various <b>ldap_modrdn</b> functions allow you to change only the relative distinguished name, which is the least significant component of the object's distinguished name. Effective with version 3, LDAP provides the Modify Distinguished Name protocol operation that allows more general name change access. This feature is available by calling 
<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a> or 
<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a>. These functions are  recommended, instead of the <b>ldap_modrdn</b> function, to change an entry name.

Multithreading: Calls to <b>ldap_modrdn</b> are thread-safe, provided that 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting other operations. <b>ldap_modrdn</b> is obsolete and provided solely for compatibility with LDAP 1 implementations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/7bf7370f-a5e6-474e-8fe9-e6895ef48ab5">ldap_modrdn2</a>



<a href="https://msdn.microsoft.com/a2cf121d-4e84-4195-9080-3b6c0c4cea82">ldap_modrdn2_s</a>



<a href="https://msdn.microsoft.com/0ea0c52d-5056-4ccf-bc64-87a2f0ebd0c5">ldap_modrdn_s</a>



<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a>



<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 


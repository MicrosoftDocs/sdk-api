---
UID: NF:winldap.ldap_modrdn2
title: ldap_modrdn2 function
author: windows-sdk-content
description: The ldap_modrdn2 function changes the relative distinguished name of an LDAP entry.
old-location: ldap\ldap_modrdn2.htm
old-project: LDAP
ms.assetid: 7bf7370f-a5e6-474e-8fe9-e6895ef48ab5
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_modrdn2, ldap.ldap__modrdn2, ldap.ldap_modrdn2, ldap_modrdn2, ldap_modrdn2 function [LDAP], ldap_modrdn2A, ldap_modrdn2W, winldap/ldap_modrdn2, winldap/ldap_modrdn2A, winldap/ldap_modrdn2W"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_modrdn2W (Unicode) and ldap_modrdn2A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_modrdn2
 - ldap_modrdn2A
 - ldap_modrdn2W
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_modrdn2 function


## -description


The <b>ldap_modrdn2</b> function changes the relative distinguished name of an LDAP entry.

This function is obsolete. For LDAP 3 or later, use the 
<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a> or 
<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a> functions.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param DistinguishedName [in]

A null-terminated string that contains the distinguished name to change.


### -param NewDistinguishedName [in]

A null-terminated string that contains the new relative distinguished name to give the entry.


### -param DeleteOldRdn [in]

<b>TRUE</b> if the old relative distinguished name should be deleted; <b>FALSE</b> if the old relative distinguished name should be retained.


## -returns



If the function succeeds, it returns the message ID of the modify operation.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.




## -remarks



Use the <b>ldap_modrdn2</b> function, or its synchronous equivalent, 
<a href="https://msdn.microsoft.com/a2cf121d-4e84-4195-9080-3b6c0c4cea82">ldap_modrdn2_s</a>, to change the name of an LDAP entry.

As an asynchronous function, <b>ldap_modrdn2</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous add operation before it has completed, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

Be aware  that the various <a href="https://msdn.microsoft.com/7a85eb4d-dcb1-4a5b-a7df-1d726215bde3">ldap_modrdn</a> functions enable you to change only the relative distinguished name, which is the least significant component of the object's distinguished name. Effective with version 3, LDAP provides the Modify Distinguished Name protocol operation, which enables more general name-change access. This functionality is available by calling 
<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a> or 
<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a>. These functions are recommended, instead of the <b>ldap_modrdn2</b> function, to change an entry name.

Multithreading: Calls to <b>ldap_modrdn2</b> are thread-safe, provided that 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the <a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or <a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/a2cf121d-4e84-4195-9080-3b6c0c4cea82">ldap_modrdn2_s</a>



<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a>



<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 


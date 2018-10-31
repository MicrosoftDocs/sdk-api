---
UID: NF:winldap.ldap_modifyA
title: ldap_modifyA function
author: windows-sdk-content
description: The ldap_modify function changes an existing entry.
old-location: ldap\ldap_modify.htm
tech.root: ldap
ms.assetid: 93ae0af4-1b16-4bb0-952f-139241189d79
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_ldap_ldap_modify, ldap.ldap__modify, ldap.ldap_modify, ldap_modify, ldap_modify function [LDAP], ldap_modifyA, ldap_modifyW, winldap/ldap_modify, winldap/ldap_modifyA, winldap/ldap_modifyW"
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
req.unicode-ansi: ldap_modifyW (Unicode) and ldap_modifyA (ANSI)
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
 - ldap_modify
 - ldap_modifyA
 - ldap_modifyW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_modifyA function


## -description


The <b>ldap_modify</b> function changes an existing entry.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the name of the entry to modify.


### -param mods [in]

A null-terminated array of modifications to make to the entry.


## -returns



If the function succeeds, it returns the message ID of the modify operation.

If the function fails, it returns –1 and sets the session error parameters in the 
<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> data structure.




## -remarks



The <b>ldap_modify</b> function initiates an asynchronous operation to modify an existing entry. If values are being added to or replaced in the entry, the function creates the attribute, if necessary. If values are being deleted, and no values remain, the function removes the attribute. All modifications are performed in the order in which they are listed.

As an asynchronous function, <b>ldap_modify</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous operation before it has completed, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

If you prefer to have the function return the results directly, use the synchronous routine 
<a href="https://msdn.microsoft.com/26002d58-a4ac-4fd6-aa63-39210f8fc883">ldap_modify_s</a>. Use 
<a href="https://msdn.microsoft.com/a11f4944-d574-4215-a25e-536adf21c469">ldap_modify_ext</a> or 
<a href="https://msdn.microsoft.com/d71190d6-4775-4f37-b509-3395a7352272">ldap_modify_ext_s</a> if you need support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_modify</b> are thread-safe, provided that 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines) before attempting any other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/a11f4944-d574-4215-a25e-536adf21c469">ldap_modify_ext</a>



<a href="https://msdn.microsoft.com/d71190d6-4775-4f37-b509-3395a7352272">ldap_modify_ext_s</a>



<a href="https://msdn.microsoft.com/26002d58-a4ac-4fd6-aa63-39210f8fc883">ldap_modify_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 


---
UID: NF:winldap.ldap_addW
title: ldap_addW function
author: windows-sdk-content
description: Initiates an asynchronous add operation to a directory tree.
old-location: ldap\ldap_add.htm
old-project: LDAP
ms.assetid: d978f668-7726-44e4-a0b1-31390e8498c4
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_add, ldap.ldap__add, ldap.ldap_add, ldap_add, ldap_add function [LDAP], ldap_addA, ldap_addW, winldap/ldap_add, winldap/ldap_addA, winldap/ldap_addW"
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
req.unicode-ansi: ldap_addW (Unicode) and ldap_addA (ANSI)
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
 - ldap_add
 - ldap_addA
 - ldap_addW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_addW function


## -description


The <b>ldap_add</b> function initiates an asynchronous add operation to a directory tree. For an add operation to succeed, the parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root).


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.


### -param attrs [in]

An array of pointers to 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Each structure specifies a single attribute.


## -returns



If the function succeeds, the message ID of the add operation is returned.

If the function fails, it returns –1 and sets the session error parameters in the 
<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> data structure. To retrieve the error data, use <a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a>.




## -remarks



Before calling <b>ldap_add</b>, create an entry by specifying its attributes in 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Set the <b>mod_op</b> member of each structure to LDAP_MOD_ADD, and set the <b>mod_type</b> and <b>mod_vals</b> members as appropriate for your entry.

As an asynchronous function, <b>ldap_add</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous add operation before it has been completed, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

To have the results returned directly, use the synchronous function 
<a href="https://msdn.microsoft.com/83ad8c35-92c4-4d73-93f5-f470655e8db5">ldap_add_s</a>. Use 
<a href="https://msdn.microsoft.com/13ad97e7-6d3c-43a6-b806-ec775abe303c">ldap_add_ext</a> or 
<a href="https://msdn.microsoft.com/b124ad29-2f9a-48c4-b51e-2fc9143a630c">ldap_add_ext_s</a> to enable support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_add</b> are thread-safe, provided that 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/97d7cd88-7fa8-40d6-9ea1-f2e586634a28">Synchronous and Asynchronous Calls</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/13ad97e7-6d3c-43a6-b806-ec775abe303c">ldap_add_ext</a>



<a href="https://msdn.microsoft.com/b124ad29-2f9a-48c4-b51e-2fc9143a630c">ldap_add_ext_s</a>



<a href="https://msdn.microsoft.com/83ad8c35-92c4-4d73-93f5-f470655e8db5">ldap_add_s</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 


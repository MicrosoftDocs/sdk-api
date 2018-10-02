---
UID: NF:winldap.ldap_add_sW
title: ldap_add_sW function
author: windows-sdk-content
description: The ldap_add_s function initiates a synchronous add operation that adds an entry to a tree. The parent of the entry being added must already exist or the parent must be empty (equal to the root distinguished name) for an add operation to succeed.
old-location: ldap\ldap_add_s.htm
tech.root: LDAP
ms.assetid: 83ad8c35-92c4-4d73-93f5-f470655e8db5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "_ldap_ldap_add_s, ldap.ldap__add__s, ldap.ldap_add_s, ldap_add_s, ldap_add_s function [LDAP], ldap_add_sA, ldap_add_sW, winldap/ldap_add_s, winldap/ldap_add_sA, winldap/ldap_add_sW"
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
req.unicode-ansi: ldap_add_sW (Unicode) and ldap_add_sA (ANSI)
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
 - ldap_add_s
 - ldap_add_sA
 - ldap_add_sW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_add_sW function


## -description


The <b>ldap_add_s</b> function initiates a synchronous add operation that adds an entry to a tree. The parent of the entry being added must already exist or the parent must be empty (equal to the root distinguished name) for an add operation to succeed.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.


### -param attrs [in]

A null-terminated array of pointers to 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Each structure specifies a single attribute. See Remarks for more information.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



Before calling <b>ldap_add_s</b>. you must create an entry by specifying its attributes in 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Set the <b>mod_op</b> member of each structure to LDAP_MOD_ADD, and set the <b>mod_type</b> and <b>mod_vals</b> members as appropriate for your entry. See 
<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a> for more information.

Upon completion of the add operation, <b>ldap_add_s</b> returns to the caller. Use 
<a href="https://msdn.microsoft.com/d978f668-7726-44e4-a0b1-31390e8498c4">ldap_add</a> if you prefer to have the operation carried out asynchronously.

Multithreading: Calls to <b>ldap_add_s</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines) before attempting any other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/d978f668-7726-44e4-a0b1-31390e8498c4">ldap_add</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 


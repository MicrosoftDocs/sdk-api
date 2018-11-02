---
UID: NF:winldap.ldap_add_ext_sW
title: ldap_add_ext_sW function
author: windows-sdk-content
description: The ldap_add_ext_s function initiates a synchronous add operation to a tree. For an add operation to succeed, the parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root).
old-location: ldap\ldap_add_ext_s.htm
tech.root: ldap
ms.assetid: b124ad29-2f9a-48c4-b51e-2fc9143a630c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_ldap_ldap_add_ext_s, ldap.ldap__add__ext__s, ldap.ldap_add_ext_s, ldap_add_ext_s, ldap_add_ext_s function [LDAP], ldap_add_ext_sA, ldap_add_ext_sW, winldap/ldap_add_ext_s, winldap/ldap_add_ext_sA, winldap/ldap_add_ext_sW"
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
req.unicode-ansi: ldap_add_ext_sW (Unicode) and ldap_add_ext_sA (ANSI)
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
 - ldap_add_ext_s
 - ldap_add_ext_sA
 - ldap_add_ext_sW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_add_ext_sW function


## -description


The <b>ldap_add_ext_s</b> function initiates a synchronous add operation to a tree. For an add operation to succeed, the parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root).


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.


### -param attrs [in]

An array of pointers to 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Each structure specifies a single attribute. For more information, see the  Remarks section.


### -param ServerControls [in]

A list of LDAP server controls.


### -param ClientControls [in]

A list of client controls.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see <a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The parameters and effects of <b>ldap_add_ext_s</b> include those of 
<a href="https://msdn.microsoft.com/83ad8c35-92c4-4d73-93f5-f470655e8db5">ldap_add_s</a>. The extended routine includes additional parameters to support client and server controls.

Before calling <b>ldap_add_ext_s</b>, create an entry by specifying its attributes in 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Set the <b>mod_op</b> member of the each structure to <b>LDAP_MOD_ADD</b>, and set the <b>mod_type</b> and <b>mod_vals</b> members as appropriate for your entry.

Upon completion of the add operation, <b>ldap_add_ext_s</b> returns to the caller. Use 
<a href="https://msdn.microsoft.com/13ad97e7-6d3c-43a6-b806-ec775abe303c">ldap_add_ext</a> if you prefer to have the operation completed asynchronously.

Multithreading: Calls to <b>ldap_add_ext_s</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>
<i>ServerControls</i> and <i>ClientControls</i> are optional and should be set to <b>NULL</b> if not used.




## -see-also




<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/13ad97e7-6d3c-43a6-b806-ec775abe303c">ldap_add_ext</a>



<a href="https://msdn.microsoft.com/83ad8c35-92c4-4d73-93f5-f470655e8db5">ldap_add_s</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 


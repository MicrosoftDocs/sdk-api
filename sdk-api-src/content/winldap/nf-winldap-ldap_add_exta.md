---
UID: NF:winldap.ldap_add_extA
title: ldap_add_extA function
author: windows-sdk-content
description: The ldap_add_ext function initiates an asynchronous add operation to a tree. The parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root) for an add operation to succeed.
old-location: ldap\ldap_add_ext.htm
tech.root: LDAP
ms.assetid: 13ad97e7-6d3c-43a6-b806-ec775abe303c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_ldap_ldap_add_ext, ldap.ldap__add__ext, ldap.ldap_add_ext, ldap_add_ext, ldap_add_ext function [LDAP], ldap_add_extA, ldap_add_extW, winldap/ldap_add_ext, winldap/ldap_add_extA, winldap/ldap_add_extW"
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
req.unicode-ansi: ldap_add_extW (Unicode) and ldap_add_extA (ANSI)
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
 - ldap_add_ext
 - ldap_add_extA
 - ldap_add_extW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_add_extA
: 
---

# ldap_add_extA function


## -description


The <b>ldap_add_ext</b> function initiates an asynchronous add operation to a tree. The parent of the entry added must exist, or the parent must be empty (equal to the distinguished name of the root) for an add operation to succeed.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to add.


### -param attrs [in]

An array of pointers to 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Each structure specifies a single attribute. For more information, see the Remarks section.


### -param ServerControls [in]

List of LDAP server controls.


### -param ClientControls [in]

List of client controls.


### -param MessageNumber [out]

The message ID for the request.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see <a href="functions.htm">Error Handling</a>.




## -remarks



The parameters and effects of <b>ldap_add_ext</b> includes those of 
<a href="https://msdn.microsoft.com/d978f668-7726-44e4-a0b1-31390e8498c4">ldap_add</a>. The extended routine includes additional parameters to support client and server controls and thread safety.

Before calling <b>ldap_add_ext</b>, create an entry by specifying its attributes in 
<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a> structures. Set the <b>mod_op</b> field of each structure to <b>LDAP_MOD_ADD</b>, and set the <b>mod_type</b> and <b>mod_vals</b> fields as appropriate for your entry.

If the operation succeeds, <b>ldap_add_ext</b> passes the message ID to the caller as a parameter. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation.

To have the results returned directly, use the synchronous function 
<a href="https://msdn.microsoft.com/b124ad29-2f9a-48c4-b51e-2fc9143a630c">ldap_add_ext_s</a>.

Multithreaded: Calls to <b>ldap_add_ext</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>
<i>ServerControls</i> and <i>ClientControls</i> are optional and should be set to <b>NULL</b> if not used.




## -see-also




<a href="functions.htm">Error Handling</a>



<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



Functions



<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/d978f668-7726-44e4-a0b1-31390e8498c4">ldap_add</a>



<a href="https://msdn.microsoft.com/b124ad29-2f9a-48c4-b51e-2fc9143a630c">ldap_add_ext_s</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 


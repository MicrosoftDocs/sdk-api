---
UID: NF:winldap.ldap_delete_ext_sA
title: ldap_delete_ext_sA function
author: windows-sdk-content
description: The ldap_delete_ext_s function is an extended routine that performs a synchronous operation to remove a leaf entry from the directory tree.
old-location: ldap\ldap_delete_ext_s.htm
tech.root: ldap
ms.assetid: eb00a5c1-b7b8-4b68-9d91-d52235f5e1ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_delete_ext_s, ldap.ldap__delete__ext__s, ldap.ldap_delete_ext_s, ldap_delete_ext_s, ldap_delete_ext_s function [LDAP], ldap_delete_ext_sA, ldap_delete_ext_sW, winldap/ldap_delete_ext_s, winldap/ldap_delete_ext_sA, winldap/ldap_delete_ext_sW"
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
req.unicode-ansi: ldap_delete_ext_sW (Unicode) and ldap_delete_ext_sA (ANSI)
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
 - ldap_delete_ext_s
 - ldap_delete_ext_sA
 - ldap_delete_ext_sW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_delete_ext_sA function


## -description


The <b>ldap_delete_ext_s</b> function is an extended routine that performs a synchronous operation to remove a leaf entry from the directory tree.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.


### -param ServerControls [in]

Optional. List of LDAP server controls. Set this parameter to <b>NULL</b> if not used.


### -param ClientControls [in]

Optional. List of client controls. Set this parameter to <b>NULL</b> if not used.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Call <b>ldap_delete_ext_s</b> to remove a leaf entry from the directory tree. LDAP does not support deletion of entire subtrees in a single operation, however there is an extended control, <a href="https://msdn.microsoft.com/b47a0f40-7191-40a5-a914-6c4fa78df8cb">LDAP_SERVER_TREE_DELETE_OID</a>, that does provide this. The parameters and effects of <b>ldap_delete_ext_s</b> include those of 
<a href="https://msdn.microsoft.com/cded1b76-0fad-454f-bf5a-c500c9079f08">ldap_delete_s</a>. The extended routine includes additional parameters to support client and server controls and thread safety.

As a synchronous function, <b>ldap_delete_ext_s</b> returns when the delete operation is complete. Use 
<a href="https://msdn.microsoft.com/314f3128-ab09-45a7-a678-779d5b7d4d72">ldap_delete</a> or 
<a href="https://msdn.microsoft.com/65c4fa7c-76d8-47ec-b5c5-bf671529f5f1">ldap_delete_ext</a> to have the delete operation performed asynchronously.

Multithreading: Calls to <b>ldap_delete_ext_s</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/314f3128-ab09-45a7-a678-779d5b7d4d72">ldap_delete</a>



<a href="https://msdn.microsoft.com/65c4fa7c-76d8-47ec-b5c5-bf671529f5f1">ldap_delete_ext</a>



<a href="https://msdn.microsoft.com/cded1b76-0fad-454f-bf5a-c500c9079f08">ldap_delete_s</a>
 

 


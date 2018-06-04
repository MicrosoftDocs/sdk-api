---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ldap_delete_ext_sW function


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



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/314f3128-ab09-45a7-a678-779d5b7d4d72">ldap_delete</a>



<a href="https://msdn.microsoft.com/65c4fa7c-76d8-47ec-b5c5-bf671529f5f1">ldap_delete_ext</a>



<a href="https://msdn.microsoft.com/cded1b76-0fad-454f-bf5a-c500c9079f08">ldap_delete_s</a>
 

 


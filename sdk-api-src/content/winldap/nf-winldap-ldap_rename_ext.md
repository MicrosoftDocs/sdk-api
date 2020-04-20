---
UID: NF:winldap.ldap_rename_ext
title: ldap_rename_ext function (winldap.h)
description: The ldap_rename_ext function starts an asynchronous operation that changes the distinguished name of an entry in the directory. This function is available effective with LDAP 3.helpviewer_keywords: ["_ldap_ldap_rename_ext","ldap.ldap__rename__ext","ldap.ldap_rename_ext","ldap_rename_ext","ldap_rename_ext function [LDAP]","ldap_rename_extA","ldap_rename_extW","winldap/ldap_rename_ext","winldap/ldap_rename_extA","winldap/ldap_rename_extW"]
old-location: ldap\ldap_rename_ext.htm
tech.root: ldap
ms.assetid: 73633a71-ebe6-4169-a9ff-17151d90ebcd
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_rename_ext, ldap.ldap__rename__ext, ldap.ldap_rename_ext, ldap_rename_ext, ldap_rename_ext function [LDAP], ldap_rename_extA, ldap_rename_extW, winldap/ldap_rename_ext, winldap/ldap_rename_extA, winldap/ldap_rename_extW
f1_keywords:
- winldap/ldap_rename_ext
dev_langs:
- c++
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_rename_extW (Unicode) and ldap_rename_extA (ANSI)
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
- ldap_rename_ext
- ldap_rename_extA
- ldap_rename_extW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_rename_ext function


## -description


The <b>ldap_rename_ext</b> function starts an asynchronous operation that changes the distinguished name of an entry in the directory. This function is available effective with LDAP 3.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a wide, null-terminated string that contains the distinguished name of the entry to be renamed.


### -param NewRDN [in]

A pointer to a wide, null-terminated string that contains the new relative distinguished name for the entry.


### -param NewParent [in]

A pointer to a wide, null-terminated string that contains the distinguished name of the new parent for this entry. This parameter enables you to move the entry to a new parent container.


### -param DeleteOldRdn [in]

<b>TRUE</b> if the old relative distinguished name should be deleted; <b>FALSE</b> if the old relative distinguished name should be retained.


### -param ServerControls [in]

List of LDAP server controls.


### -param ClientControls [in]

List of client controls.


### -param MessageNumber [out]

Pointer to a variable that receives the message identifier for this asynchronous operation. Use this identifier with the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> function to retrieve the results of the operation.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.




## -remarks



This function provides extended renaming operations. For example, you can pass controls that separate the parent from the relative distinguished name, for clarity.

Multithreading: Calls to <b>ldap_rename_ext</b> are thread-safe.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>
 

 


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

# ldap_modrdn_sW function


## -description


The <b>ldap_modrdn_s</b> function changes the relative distinguished name of an LDAP entry.

This function is obsolete and is provided for backward compatibility with earlier versions of LDAP. For LDAP 3 or later, use the 
<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a> or 
<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a> function.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param DistinguishedName [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to be changed.


### -param NewDistinguishedName [out]

A pointer to a null-terminated string that contains the new relative distinguished name to give the entry.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Use the <b>ldap_modrdn_s</b> function, or its asynchronous equivalent, 
<a href="https://msdn.microsoft.com/7a85eb4d-dcb1-4a5b-a7df-1d726215bde3">ldap_modrdn</a>, to change the name of an LDAP entry. This function provides compatibility with LDAP 1. Otherwise, use 
<a href="https://msdn.microsoft.com/7bf7370f-a5e6-474e-8fe9-e6895ef48ab5">ldap_modrdn2</a> or 
<a href="https://msdn.microsoft.com/a2cf121d-4e84-4195-9080-3b6c0c4cea82">ldap_modrdn2_s</a>.

Be aware that the <a href="https://msdn.microsoft.com/7a85eb4d-dcb1-4a5b-a7df-1d726215bde3">ldap_modrdn</a> functions enable you to change only the relative distinguished name, which is the least significant component of the object's distinguished name. Effective with version 3, LDAP provides the Modify Distinguished Name protocol operation that allows more general name change access. This feature is available by calling 
<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a> or 
<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a>. These functions are  recommended, instead of the <b>ldap_modrdn_s</b> function, to change an entry name.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/7a85eb4d-dcb1-4a5b-a7df-1d726215bde3">ldap_modrdn</a>



<a href="https://msdn.microsoft.com/7bf7370f-a5e6-474e-8fe9-e6895ef48ab5">ldap_modrdn2</a>



<a href="https://msdn.microsoft.com/a2cf121d-4e84-4195-9080-3b6c0c4cea82">ldap_modrdn2_s</a>



<a href="https://msdn.microsoft.com/73633a71-ebe6-4169-a9ff-17151d90ebcd">ldap_rename_ext</a>



<a href="https://msdn.microsoft.com/85a605f9-d075-4b1d-bfcb-a75c9e7f3023">ldap_rename_ext_s</a>
 

 


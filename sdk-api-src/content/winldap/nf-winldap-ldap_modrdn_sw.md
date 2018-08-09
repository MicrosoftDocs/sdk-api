---
UID: NF:winldap.ldap_modrdn_sW
title: ldap_modrdn_sW function
author: windows-sdk-content
description: Changes the relative distinguished name of an LDAP entry.
old-location: ldap\ldap_modrdn_s.htm
old-project: ldap
ms.assetid: 0ea0c52d-5056-4ccf-bc64-87a2f0ebd0c5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_modrdn_s, ldap.ldap__modrdn__s, ldap.ldap_modrdn_s, ldap_modrdn_s, ldap_modrdn_s function [LDAP], ldap_modrdn_sA, ldap_modrdn_sW, winldap/ldap_modrdn_s, winldap/ldap_modrdn_sA, winldap/ldap_modrdn_sW"
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
req.unicode-ansi: ldap_modrdn_sW (Unicode) and ldap_modrdn_sA (ANSI)
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
 - ldap_modrdn_s
 - ldap_modrdn_sA
 - ldap_modrdn_sW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 


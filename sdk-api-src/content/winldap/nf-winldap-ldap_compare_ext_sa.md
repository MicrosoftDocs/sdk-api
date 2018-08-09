---
UID: NF:winldap.ldap_compare_ext_sA
title: ldap_compare_ext_sA function
author: windows-sdk-content
description: Use the ldap_compare_ext_s function to determine if an attribute, for a given entry, holds a known value.
old-location: ldap\ldap_compare_ext_s.htm
old-project: ldap
ms.assetid: b22568b1-5043-422e-9c4e-cc51cc77d143
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_compare_ext_s, ldap.ldap__compare__ext__s, ldap.ldap_compare_ext_s, ldap_compare_ext_s, ldap_compare_ext_s function [LDAP], ldap_compare_ext_sA, ldap_compare_ext_sW, winldap/ldap_compare_ext_s, winldap/ldap_compare_ext_sA, winldap/ldap_compare_ext_sW"
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
req.unicode-ansi: ldap_compare_ext_sW (Unicode) and ldap_compare_ext_sA (ANSI)
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
 - ldap_compare_ext_s
 - ldap_compare_ext_sA
 - ldap_compare_ext_sW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_compare_ext_sA function


## -description


Use the <b>ldap_compare_ext_s</b> function to determine if an attribute, for a given entry, holds a known value.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to compare.


### -param Attr [in]

A pointer to a null-terminated string that contains the attribute to compare.


### -param Value [in]

A pointer to a null-terminated string that contains the string attribute value to be compared to the attribute value. Set to <b>NULL</b> if not used.


### -param Data [in]

The 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> attribute value to be compared to the attribute value. Set to <b>NULL</b> if not used.


### -param ServerControls [in]

Optional. A list of LDAP server controls. Set to <b>NULL</b> if not used.


### -param ClientControls [in]

Optional. A list of LDAP client controls. Set to <b>NULL</b> if not used.


## -returns



If the function succeeds, and the attribute and known values match, <b>LDAP_COMPARE_TRUE</b> is returned; if the values do not match, <b>LDAP_COMPARE_FALSE</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_compare_ext_s</b> function initiates a synchronous compare operation, comparing the value of an attribute to a known value. The parameters and effects of <b>ldap_compare_ext_s</b> subsume those of 
<a href="https://msdn.microsoft.com/44a7001d-d7ad-4b29-80bf-8d4b06e0fa43">ldap_compare_s</a>. The extended routine includes additional parameters to support client and server controls, and comparison of binary values.

Use the <i>Value</i> parameter for comparing string values or use the <i>Data</i> parameter for comparing raw binary data. Set the unused parameter to <b>NULL</b>. If neither parameter is <b>NULL</b>, the compare operation will use the value in the <i>Data</i> parameter.

Multithreading: Calls to <b>ldap_compare_ext_s</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>



<a href="https://msdn.microsoft.com/44a7001d-d7ad-4b29-80bf-8d4b06e0fa43">ldap_compare_s</a>
 

 


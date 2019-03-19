---
UID: NF:winldap.ldap_parse_referenceW
title: ldap_parse_referenceW function (winldap.h)
author: windows-sdk-content
description: The ldap_parse_reference function returns a list of subordinate referrals in a search response message.
old-location: ldap\ldap_parse_reference.htm
tech.root: ldap
ms.assetid: 106db7dd-ee1e-48c9-9357-e14d4f8e8782
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_parse_reference, ldap.ldap__parse__reference, ldap.ldap_parse_reference, ldap_parse_reference, ldap_parse_reference function [LDAP], ldap_parse_referenceA, ldap_parse_referenceW, winldap/ldap_parse_reference, winldap/ldap_parse_referenceA, winldap/ldap_parse_referenceW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_parse_referenceW (Unicode) and ldap_parse_referenceA (ANSI)
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
 - ldap_parse_reference
 - ldap_parse_referenceA
 - ldap_parse_referenceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_parse_referenceW function


## -description


The <b>ldap_parse_reference</b> function returns a list of subordinate referrals in a search response message.


## -parameters




### -param Connection [in]

The session handle.


### -param ResultMessage [in]

A pointer to an 
<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a> structure containing the search response.


### -param Referrals [out]

A pointer to the list of subordinate referrals. Free with <a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



The <b>ldap_parse_reference</b> function returns a list of referrals in the form of URLs. Call this function if a call to 
<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a> indicates that there are referrals.

When it is no longer needed, free the <i>Referrals</i> pointer by calling 
<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>



<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>



<a href="https://msdn.microsoft.com/67c9f04c-4b8e-4e97-902d-fceccf27f522">ldap_value_free</a>
 

 


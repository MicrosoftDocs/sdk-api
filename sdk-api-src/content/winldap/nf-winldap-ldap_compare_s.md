---
UID: NF:winldap.ldap_compare_s
title: ldap_compare_s function
author: windows-sdk-content
description: Use the ldap_compare_s function to determine whether an attribute for a given entry holds a known value.
old-location: ldap\ldap_compare_s.htm
tech.root: LDAP
ms.assetid: 44a7001d-d7ad-4b29-80bf-8d4b06e0fa43
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_ldap_ldap_compare_s, ldap.ldap__compare__s, ldap.ldap_compare_s, ldap_compare_s, ldap_compare_s function [LDAP], ldap_compare_sA, ldap_compare_sW, winldap/ldap_compare_s, winldap/ldap_compare_sA, winldap/ldap_compare_sW"
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
req.unicode-ansi: ldap_compare_sW (Unicode) and ldap_compare_sA (ANSI)
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
 - ldap_compare_s
 - ldap_compare_sA
 - ldap_compare_sW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_compare_s
: 
---

# ldap_compare_s function


## -description


Use the <b>ldap_compare_s</b> function to determine whether 
    an attribute for a given entry holds a known value.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry.


### -param attr [in]

A pointer to a null-terminated string that contains the attribute to compare.


### -param value [in]

A pointer to a null-terminated string that contains the string attribute value to compare to the attribute 
      value.


## -returns



If the function succeeds, and the attribute and known values match, the return value is 
       <b>LDAP_COMPARE_TRUE</b>. If the values do not match, the return value is 
       <b>LDAP_COMPARE_FALSE</b>.

If the function fails, it returns an error code. See 
       <a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



The <b>ldap_compare_s</b> function initiates a synchronous 
    compare operation, comparing the value of an attribute to a known string value. Use 
    <a href="https://msdn.microsoft.com/b22568b1-5043-422e-9c4e-cc51cc77d143">ldap_compare_ext_s</a> if you need to compare binary 
    values. Use <a href="https://msdn.microsoft.com/0cdcea2f-5ee2-407a-a229-5a3fb1e3b856">ldap_compare</a> or 
    <a href="https://msdn.microsoft.com/07e96a95-439b-4bb1-a9ca-d76d181e8bea">ldap_compare_ext</a> to carry out an asynchronous compare 
    operation.

Multithreading: Calls to <b>ldap_compare_s</b> are 
    thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
    <a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
    <a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines) before attempting any 
    other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/0cdcea2f-5ee2-407a-a229-5a3fb1e3b856">ldap_compare</a>



<a href="https://msdn.microsoft.com/07e96a95-439b-4bb1-a9ca-d76d181e8bea">ldap_compare_ext</a>



<a href="https://msdn.microsoft.com/b22568b1-5043-422e-9c4e-cc51cc77d143">ldap_compare_ext_s</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 


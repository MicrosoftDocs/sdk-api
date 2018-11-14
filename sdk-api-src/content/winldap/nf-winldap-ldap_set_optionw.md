---
UID: NF:winldap.ldap_set_optionW
title: ldap_set_optionW function
author: windows-sdk-content
description: Sets options on connection blocks.
old-location: ldap\ldap_set_option.htm
tech.root: ldap
ms.assetid: b6d6b285-7302-4812-bbcb-0aeb5b53cf23
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_ldap_ldap_set_option, ldap.ldap__set__option, ldap.ldap_set_option, ldap_set_option, ldap_set_option function [LDAP], ldap_set_optionW, winldap/ldap_set_option, winldap/ldap_set_optionW"
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
req.unicode-ansi: ldap_set_optionW (Unicode) and ldap_set_option (ANSI)
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
 - ldap_set_option
 - ldap_set_option
 - ldap_set_optionW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_set_optionW
: 
---

# ldap_set_optionW function


## -description


The <b>ldap_set_option</b> function sets options on connection blocks. For more information about structures, see 
<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>.


## -parameters




### -param ld [in]

The session handle.


### -param option [in]

The name of the option set.


### -param invalue [in]

A pointer to the value that the option is to be given. The actual type of this parameter depends on the setting of the option parameter. The constants LDAP_OPT_ON and LDAP_OPT_OFF can be given for options that have on or off settings.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Call <b>ldap_set_option</b> to access the 
<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> structure that represents an LDAP session. Do not attempt to modify the LDAP data structure directly.

For more information and  a description of optional settings that apply to an LDAP session, see 
<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>. For more information about flags, see 
<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>.

It is now possible to digitally sign or encrypt all of your LDAP traffic to and from a Windows LDAP server using the Kerberos authentication protocol. This new feature provides integrity and confidentiality required by some applications. Be aware that using Secure Sockets Layer (SSL) will give you the same benefits, but requires extensive certificate enrollments for the server and, sometimes, for the client.

To enable signing and sealing, you have to turn on one of the following options prior to calling <a href="https://msdn.microsoft.com/67d30a7b-2f42-4e1a-8c59-5ba22ed3fad4">ldap_bind_s</a> with <b>LDAP_AUTH_NEGOTIATE</b> for the bind method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define LDAP_OPT_SIGN      0x95
#define LDAP_OPT_ENCRYPT   0x96</pre>
</td>
</tr>
</table></span></div>
To turn off signing and sealing, close the connection by calling <a href="https://msdn.microsoft.com/5d8b3198-3935-4305-b0f1-eaf1a9355cf3">ldap_unbind()</a> on the connection handle.

Multithreading: Calls to <b>ldap_set_option</b> are unsafe because it affects the connection as a whole. Use caution if threads share connections.




## -see-also




<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/1447d242-b8db-4b7e-9871-2193f747be4e">Getting and Setting Session Options</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/e07c2c3d-8099-4f9c-9ee7-26c1287110d5">ldap_get_option</a>
 

 


---
UID: NF:winldap.ldap_set_optionW
title: ldap_set_optionW function (winldap.h)
description: The ldap_set_optionW (Unicode) function (winldap.h) sets options on connection blocks. 
helpviewer_keywords: ["_ldap_ldap_set_option","ldap.ldap__set__option","ldap.ldap_set_option","ldap_set_option","ldap_set_option function [LDAP]","ldap_set_optionW","winldap/ldap_set_option","winldap/ldap_set_optionW"]
old-location: ldap\ldap_set_option.htm
tech.root: ldap
ms.assetid: b6d6b285-7302-4812-bbcb-0aeb5b53cf23
ms.date: 08/04/2022
ms.keywords: _ldap_ldap_set_option, ldap.ldap__set__option, ldap.ldap_set_option, ldap_set_option, ldap_set_option function [LDAP], ldap_set_optionW, winldap/ldap_set_option, winldap/ldap_set_optionW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_set_optionW
 - winldap/ldap_set_optionW
dev_langs:
 - c++
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
---

# ldap_set_optionW function


## -description

The <b>ldap_set_option</b> function sets options on connection blocks. For more information about structures, see 
<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>.

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
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Call <b>ldap_set_option</b> to access the 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a> structure that represents an LDAP session. Do not attempt to modify the LDAP data structure directly.

For more information and  a description of optional settings that apply to an LDAP session, see 
<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>. For more information about flags, see 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>.

It is now possible to digitally sign or encrypt all of your LDAP traffic to and from a Windows LDAP server using the Kerberos authentication protocol. This new feature provides integrity and confidentiality required by some applications. Be aware that using Secure Sockets Layer (SSL) will give you the same benefits, but requires extensive certificate enrollments for the server and, sometimes, for the client.

To enable signing and sealing, you have to turn on one of the following options prior to calling <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_bind_s">ldap_bind_s</a> with <b>LDAP_AUTH_NEGOTIATE</b> for the bind method.


```cpp
#define LDAP_OPT_SIGN      0x95
#define LDAP_OPT_ENCRYPT   0x96
```


To turn off signing and sealing, close the connection by calling <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_unbind">ldap_unbind()</a> on the connection handle.

Multithreading: Calls to <b>ldap_set_option</b> are unsafe because it affects the connection as a whole. Use caution if threads share connections.





> [!NOTE]
> The winldap.h header defines ldap_set_option as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/getting-and-setting-session-options">Getting and Setting Session Options</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>

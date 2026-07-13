---
UID: NF:winldap.ldap_get_optionW
title: ldap_get_optionW function (winldap.h)
description: The ldap_get_optionW (Unicode) function (winldap.h) retrieves the current values of session-wide parameters. 
helpviewer_keywords: ["_ldap_ldap_get_option","ldap.ldap__get__option","ldap.ldap_get_option","ldap_get_option","ldap_get_option function [LDAP]","ldap_get_optionW","winldap/ldap_get_option","winldap/ldap_get_optionW"]
old-location: ldap\ldap_get_option.htm
tech.root: ldap
ms.assetid: e07c2c3d-8099-4f9c-9ee7-26c1287110d5
ms.date: 08/03/2022
ms.keywords: _ldap_ldap_get_option, ldap.ldap__get__option, ldap.ldap_get_option, ldap_get_option, ldap_get_option function [LDAP], ldap_get_optionW, winldap/ldap_get_option, winldap/ldap_get_optionW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_get_optionW (Unicode) and ldap_get_option (ANSI)
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
 - ldap_get_optionW
 - winldap/ldap_get_optionW
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
 - ldap_get_option
 - ldap_get_option
 - ldap_get_optionW
---

# ldap_get_optionW function


## -description

The <b>ldap_get_option</b> function retrieves the current values of session-wide parameters.

## -parameters

### -param ld [in]

The session handle.

### -param option [in]

The name of the option accessed. For more information and  a list of allowable options and their values, see the following Remarks section.

### -param outvalue [out]

The address of the option value. The actual type of this parameter depends on the setting of the option parameter.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

For more information and a description of optional settings that apply to an LDAP session, see 
<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>. The <i>outvalue</i> value returns a pointer to an allocated block of memory of the type listed in the <b>Session Options</b> table; this memory should be freed using <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a> when the data is no longer required, unless it is explicitly mentioned in the <b>Session Options</b> table not to free the returned memory.

<div class="alert"><b>Note</b>  <a href="/previous-versions/windows/desktop/ldap/session-options">LDAP_OPT_ERROR_STRING</a> returns a pointer to an internal static string table, and <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a> should not be called when using this session option.</div>
<div> </div>
Multithreading: The <b>ldap_get_option</b> function is thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_get_option as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/getting-and-setting-session-options">Getting and Setting Session Options</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_set_option">ldap_set_option</a>

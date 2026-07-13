---
UID: NS:winldap.ldapapiinfoA
title: LDAPAPIInfoA (winldap.h)
description: Retrieves data about the API and implementations used. (ANSI)
helpviewer_keywords: ["LDAPAPIInfo","LDAPAPIInfo structure [LDAP]","LDAPAPIInfoA","LDAPAPIInfoW","ldap.ldapapiinfo","winldap/LDAPAPIInfo","winldap/LDAPAPIInfoA","winldap/LDAPAPIInfoW"]
old-location: ldap\ldapapiinfo.htm
tech.root: ldap
ms.assetid: 9175224c-82f0-4f22-9975-b1d7a332c3df
ms.date: 12/05/2018
ms.keywords: LDAPAPIInfo, LDAPAPIInfo structure [LDAP], LDAPAPIInfoA, LDAPAPIInfoW, ldap.ldapapiinfo, winldap/LDAPAPIInfo, winldap/LDAPAPIInfoA, winldap/LDAPAPIInfoW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LDAPAPIInfoW (Unicode) and LDAPAPIInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LDAPAPIInfoA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldapapiinfoA
 - winldap/ldapapiinfoA
 - LDAPAPIInfoA
 - winldap/LDAPAPIInfoA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAPAPIInfo
 - LDAPAPIInfoA
 - LDAPAPIInfoW
---

# LDAPAPIInfoA structure


## -description

The <b>LDAPAPIInfo</b> structure retrieves data about the API and implementations used.

## -struct-fields

### -field ldapai_info_version

The version of this structure, which must be set to <b>LDAP_API_INFO_VERSION</b> before a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>.

### -field ldapai_api_version

The current revision number of this LDAP API library.

### -field ldapai_protocol_version

The latest LDAP version supported by this LDAP API library.

### -field ldapai_extensions

Pointer to an array of null-terminated strings that indicate what API extensions are supported.

### -field ldapai_vendor_name

Pointer to a null-terminated string that contains the name of the API vendor.  This implementation returns the string ""Microsoft Corporation."".

### -field ldapai_vendor_version

The API vendor version number. This implementation returns an integer value in the format of MMnn, where MM is the major version number * 100, and nn is the minor version number.  For example, version 5.10 is returned as 510.

## -remarks

A pointer to this structure is passed with the <a href="/previous-versions/windows/desktop/ldap/session-options">LDAP_OPT_API_INFO</a> session option, to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>, to retrieve data about this LDAP API library.  The data returned includes a list of any API extensions supported by the implementation. When the structure data is no longer required, the caller must free the individual strings and string arrays returned in this structure by using the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a> and <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a> functions.





> [!NOTE]
> The winldap.h header defines LDAPAPIInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_memfree">ldap_memfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_value_free">ldap_value_free</a>

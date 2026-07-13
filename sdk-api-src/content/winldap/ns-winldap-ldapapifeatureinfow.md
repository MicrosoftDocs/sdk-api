---
UID: NS:winldap.ldap_apifeature_infoW
title: LDAPAPIFeatureInfoW (winldap.h)
description: Retrieves data about any supported LDAP API extensions. (Unicode)
helpviewer_keywords: ["LDAPAPIFeatureInfo","LDAPAPIFeatureInfo structure [LDAP]","LDAPAPIFeatureInfoA","LDAPAPIFeatureInfoW","ldap.ldapapifeatureinfo","winldap/LDAPAPIFeatureInfo","winldap/LDAPAPIFeatureInfoA","winldap/LDAPAPIFeatureInfoW"]
old-location: ldap\ldapapifeatureinfo.htm
tech.root: ldap
ms.assetid: c8e4a3a2-a606-49af-887d-905d67705423
ms.date: 12/05/2018
ms.keywords: LDAPAPIFeatureInfo, LDAPAPIFeatureInfo structure [LDAP], LDAPAPIFeatureInfoA, LDAPAPIFeatureInfoW, ldap.ldapapifeatureinfo, winldap/LDAPAPIFeatureInfo, winldap/LDAPAPIFeatureInfoA, winldap/LDAPAPIFeatureInfoW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LDAPAPIFeatureInfoW (Unicode) and LDAPAPIFeatureInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LDAPAPIFeatureInfoW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_apifeature_infoW
 - winldap/ldap_apifeature_infoW
 - LDAPAPIFeatureInfoW
 - winldap/LDAPAPIFeatureInfoW
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
 - LDAPAPIFeatureInfo
 - LDAPAPIFeatureInfoA
 - LDAPAPIFeatureInfoW
---

# LDAPAPIFeatureInfoW structure


## -description

The <b>LDAPAPIFeatureInfo</b> structure retrieves data about any supported LDAP API extensions.

## -struct-fields

### -field ldapaif_info_version

The version of this structure, which must be set to <b>LDAP_FEATURE_INFO_VERSION</b> before the call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a> is performed.

### -field ldapaif_name

A pointer to a null-terminated string that contains the name of the desired API extension.  This value is set before the call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a> is performed, and should match one of the strings returned in the <b>ldapai_extensions</b> member of <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapapiinfoa">LDAPAPIInfo</a> set  from a previous call to <b>ldap_get_option</b>.

### -field ldapaif_version

The vendor API extension version number.  This implementation returns an integer value in the format of MMnnn, where MM is the major version number * 1000, and nnn is the minor version number.  For example, version 1.001 would be returned as the number 1001.

## -remarks

A pointer to this structure is passed, along with the <a href="/previous-versions/windows/desktop/ldap/session-options">LDAP_FEATURE_API_INFO</a> session option and the name of the desired API extension, to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>, to retrieve detailed data about the LDAP API extension.





> [!NOTE]
> The winldap.h header defines LDAPAPIFeatureInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapapiinfoa">LDAPAPIInfo</a>



<a href="/previous-versions/windows/desktop/ldap/session-options">Session Options</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>

---
UID: NS:winldap.ldap_apifeature_infoA
title: LDAPAPIFeatureInfoA (winldap.h)

description: Retrieves data about any supported LDAP API extensions.
old-location: ldap\ldapapifeatureinfo.htm
tech.root: ldap
ms.assetid: c8e4a3a2-a606-49af-887d-905d67705423

ms.date: 12/05/2018
ms.keywords: LDAPAPIFeatureInfo, LDAPAPIFeatureInfo structure [LDAP], LDAPAPIFeatureInfoA, LDAPAPIFeatureInfoW, ldap.ldapapifeatureinfo, winldap/LDAPAPIFeatureInfo, winldap/LDAPAPIFeatureInfoA, winldap/LDAPAPIFeatureInfoW
ms.topic: struct
f1_keywords: 
 - "winldap/LDAPAPIFeatureInfo"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: LDAPAPIFeatureInfoA
req.redist: 
ms.custom: 19H1
---

# LDAPAPIFeatureInfoA structure


## -description


The <b>LDAPAPIFeatureInfo</b> structure retrieves data about any supported LDAP API extensions.


## -struct-fields




### -field ldapaif_info_version

The version of this structure, which must be set to <b>LDAP_FEATURE_INFO_VERSION</b> before the call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a> is performed.


### -field ldapaif_name

A pointer to a null-terminated string that contains the name of the desired API extension.  This value is set before the call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a> is performed, and should match one of the strings returned in the <b>ldapai_extensions</b> member of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapapiinfoa">LDAPAPIInfo</a> set  from a previous call to <b>ldap_get_option</b>.


### -field ldapaif_version

The vendor API extension version number.  This implementation returns an integer value in the format of MMnnn, where MM is the major version number * 1000, and nnn is the minor version number.  For example, version 1.001 would be returned as the number 1001.


## -remarks



A pointer to this structure is passed, along with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/session-options">LDAP_FEATURE_API_INFO</a> session option and the name of the desired API extension, to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>, to retrieve detailed data about the LDAP API extension.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapapiinfoa">LDAPAPIInfo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/session-options">Session Options</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_option">ldap_get_option</a>
 

 


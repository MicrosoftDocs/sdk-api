---
UID: NS:wincrypt._CERT_RDN_ATTR
title: CERT_RDN_ATTR (wincrypt.h)
description: Contains a single attribute of a relative distinguished name (RDN). A whole RDN is expressed in a CERT_RDN structure that contains an array of CERT_RDN_ATTR structures.
helpviewer_keywords: ["*PCERT_RDN_ATTR","CERT_RDN_ANY_TYPE","CERT_RDN_ATTR","CERT_RDN_ATTR structure [Security]","CERT_RDN_BMP_STRING","CERT_RDN_DISABLE_CHECK_TYPE_FLAG","CERT_RDN_DISABLE_IE4_UTF8_FLAG","CERT_RDN_ENABLE_PUNYCODE_FLAG","CERT_RDN_ENABLE_T61_UNICODE_FLAG","CERT_RDN_ENABLE_UTF8_UNICODE_FLAG","CERT_RDN_ENCODED_BLOB","CERT_RDN_FORCE_UTF8_UNICODE_FLAG","CERT_RDN_GENERAL_STRING","CERT_RDN_GRAPHIC_STRING","CERT_RDN_IA5_STRING","CERT_RDN_INT4_STRING","CERT_RDN_ISO646_STRING","CERT_RDN_NUMERIC_STRING","CERT_RDN_OCTET_STRING","CERT_RDN_PRINTABLE_STRING","CERT_RDN_T61_STRING","CERT_RDN_TELETEX_STRING","CERT_RDN_UNICODE_STRING","CERT_RDN_UNIVERSAL_STRING","CERT_RDN_UTF8_STRING","CERT_RDN_VIDEOTEX_STRING","CERT_RDN_VISIBLE_STRING","PCERT_RDN_ATTR","PCERT_RDN_ATTR structure pointer [Security]","_crypto2_cert_rdn_attr","security.cert_rdn_attr","szOID_AUTHORITY_REVOCATION_LIST","szOID_BUSINESS_CATEGORY","szOID_CA_CERTIFICATE","szOID_CERTIFICATE_REVOCATION_LIST","szOID_COMMON_NAME","szOID_COUNTRY_NAME","szOID_CROSS_CERTIFICATE_PAIR","szOID_DESCRIPTION","szOID_DESTINATION_INDICATOR","szOID_DEVICE_SERIAL_NUMBER","szOID_DOMAIN_COMPONENT","szOID_FACSIMILE_TELEPHONE_NUMBER","szOID_GIVEN_NAME","szOID_INITIALS","szOID_INTERNATIONAL_ISDN_NUMBER","szOID_LOCALITY_NAME","szOID_MEMBER","szOID_ORGANIZATIONAL_UNIT_NAME","szOID_ORGANIZATION_NAME","szOID_OWNER","szOID_PHYSICAL_DELIVERY_OFFICE_NAME","szOID_PKCS_12_FRIENDLY_NAME_ATTR","szOID_PKCS_12_LOCAL_KEY_ID","szOID_POSTAL_ADDRESS","szOID_POSTAL_CODE","szOID_POST_OFFICE_BOX","szOID_PREFERRED_DELIVERY_METHOD","szOID_PRESENTATION_ADDRESS","szOID_REGISTERED_ADDRESS","szOID_ROLE_OCCUPANT","szOID_RSA_emailAddr","szOID_SEARCH_GUIDE","szOID_SEE_ALSO","szOID_STATE_OR_PROVINCE_NAME","szOID_STREET_ADDRESS","szOID_SUPPORTED_APPLICATION_CONTEXT","szOID_SUR_NAME","szOID_TELEPHONE_NUMBER","szOID_TELETEXT_TERMINAL_IDENTIFIER","szOID_TELEX_NUMBER","szOID_TITLE","szOID_USER_CERTIFICATE","szOID_USER_PASSWORD","szOID_X21_ADDRESS","wincrypt/CERT_RDN_ATTR","wincrypt/PCERT_RDN_ATTR"]
old-location: security\cert_rdn_attr.htm
tech.root: security
ms.assetid: 4729e824-761c-4115-8b7b-76ffdab8ea62
ms.date: 12/05/2018
ms.keywords: '*PCERT_RDN_ATTR, CERT_RDN_ANY_TYPE, CERT_RDN_ATTR, CERT_RDN_ATTR structure [Security], CERT_RDN_BMP_STRING, CERT_RDN_DISABLE_CHECK_TYPE_FLAG, CERT_RDN_DISABLE_IE4_UTF8_FLAG, CERT_RDN_ENABLE_PUNYCODE_FLAG, CERT_RDN_ENABLE_T61_UNICODE_FLAG, CERT_RDN_ENABLE_UTF8_UNICODE_FLAG, CERT_RDN_ENCODED_BLOB, CERT_RDN_FORCE_UTF8_UNICODE_FLAG, CERT_RDN_GENERAL_STRING, CERT_RDN_GRAPHIC_STRING, CERT_RDN_IA5_STRING, CERT_RDN_INT4_STRING, CERT_RDN_ISO646_STRING, CERT_RDN_NUMERIC_STRING, CERT_RDN_OCTET_STRING, CERT_RDN_PRINTABLE_STRING, CERT_RDN_T61_STRING, CERT_RDN_TELETEX_STRING, CERT_RDN_UNICODE_STRING, CERT_RDN_UNIVERSAL_STRING, CERT_RDN_UTF8_STRING, CERT_RDN_VIDEOTEX_STRING, CERT_RDN_VISIBLE_STRING, PCERT_RDN_ATTR, PCERT_RDN_ATTR structure pointer [Security], _crypto2_cert_rdn_attr, security.cert_rdn_attr, szOID_AUTHORITY_REVOCATION_LIST, szOID_BUSINESS_CATEGORY, szOID_CA_CERTIFICATE, szOID_CERTIFICATE_REVOCATION_LIST, szOID_COMMON_NAME, szOID_COUNTRY_NAME, szOID_CROSS_CERTIFICATE_PAIR, szOID_DESCRIPTION, szOID_DESTINATION_INDICATOR, szOID_DEVICE_SERIAL_NUMBER, szOID_DOMAIN_COMPONENT, szOID_FACSIMILE_TELEPHONE_NUMBER, szOID_GIVEN_NAME, szOID_INITIALS, szOID_INTERNATIONAL_ISDN_NUMBER, szOID_LOCALITY_NAME, szOID_MEMBER, szOID_ORGANIZATIONAL_UNIT_NAME, szOID_ORGANIZATION_NAME, szOID_OWNER, szOID_PHYSICAL_DELIVERY_OFFICE_NAME, szOID_PKCS_12_FRIENDLY_NAME_ATTR, szOID_PKCS_12_LOCAL_KEY_ID, szOID_POSTAL_ADDRESS, szOID_POSTAL_CODE, szOID_POST_OFFICE_BOX, szOID_PREFERRED_DELIVERY_METHOD, szOID_PRESENTATION_ADDRESS, szOID_REGISTERED_ADDRESS, szOID_ROLE_OCCUPANT, szOID_RSA_emailAddr, szOID_SEARCH_GUIDE, szOID_SEE_ALSO, szOID_STATE_OR_PROVINCE_NAME, szOID_STREET_ADDRESS, szOID_SUPPORTED_APPLICATION_CONTEXT, szOID_SUR_NAME, szOID_TELEPHONE_NUMBER, szOID_TELETEXT_TERMINAL_IDENTIFIER, szOID_TELEX_NUMBER, szOID_TITLE, szOID_USER_CERTIFICATE, szOID_USER_PASSWORD, szOID_X21_ADDRESS, wincrypt/CERT_RDN_ATTR, wincrypt/PCERT_RDN_ATTR'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CERT_RDN_ATTR, *PCERT_RDN_ATTR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_RDN_ATTR
 - wincrypt/_CERT_RDN_ATTR
 - PCERT_RDN_ATTR
 - wincrypt/PCERT_RDN_ATTR
 - CERT_RDN_ATTR
 - wincrypt/CERT_RDN_ATTR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_RDN_ATTR
---

# CERT_RDN_ATTR structure


## -description

The <b>CERT_RDN_ATTR</b> structure contains a single attribute of a <a href="/windows/desktop/SecGloss/r-gly">relative distinguished name</a> (RDN). A whole RDN is expressed in a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structure that contains an array of <b>CERT_RDN_ATTR</b> structures.

## -struct-fields

### -field pszObjId

<a href="/windows/desktop/SecGloss/o-gly">Object identifier</a> (OID) for the type of the attribute defined in this structure. This member can be one of the following OIDs.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_AUTHORITY_REVOCATION_LIST"></a><a id="szoid_authority_revocation_list"></a><a id="SZOID_AUTHORITY_REVOCATION_LIST"></a><dl>
<dt><b>szOID_AUTHORITY_REVOCATION_LIST</b></dt>
</dl>
</td>
<td width="60%">
Security attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_BUSINESS_CATEGORY"></a><a id="szoid_business_category"></a><a id="SZOID_BUSINESS_CATEGORY"></a><dl>
<dt><b>szOID_BUSINESS_CATEGORY</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Explanatory attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_CA_CERTIFICATE"></a><a id="szoid_ca_certificate"></a><a id="SZOID_CA_CERTIFICATE"></a><dl>
<dt><b>szOID_CA_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
Security attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_CERTIFICATE_REVOCATION_LIST"></a><a id="szoid_certificate_revocation_list"></a><a id="SZOID_CERTIFICATE_REVOCATION_LIST"></a><dl>
<dt><b>szOID_CERTIFICATE_REVOCATION_LIST</b></dt>
</dl>
</td>
<td width="60%">
Security attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_COMMON_NAME"></a><a id="szoid_common_name"></a><a id="SZOID_COMMON_NAME"></a><dl>
<dt><b>szOID_COMMON_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Labeling attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_COUNTRY_NAME"></a><a id="szoid_country_name"></a><a id="SZOID_COUNTRY_NAME"></a><dl>
<dt><b>szOID_COUNTRY_NAME</b></dt>
</dl>
</td>
<td width="60%">
Two-character printable string.
Geographic attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_CROSS_CERTIFICATE_PAIR"></a><a id="szoid_cross_certificate_pair"></a><a id="SZOID_CROSS_CERTIFICATE_PAIR"></a><dl>
<dt><b>szOID_CROSS_CERTIFICATE_PAIR</b></dt>
</dl>
</td>
<td width="60%">
Security attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_DESCRIPTION"></a><a id="szoid_description"></a><a id="SZOID_DESCRIPTION"></a><dl>
<dt><b>szOID_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string. Explanatory attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_DESTINATION_INDICATOR"></a><a id="szoid_destination_indicator"></a><a id="SZOID_DESTINATION_INDICATOR"></a><dl>
<dt><b>szOID_DESTINATION_INDICATOR</b></dt>
</dl>
</td>
<td width="60%">
Printable string.
Telecommunications addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_DEVICE_SERIAL_NUMBER"></a><a id="szoid_device_serial_number"></a><a id="SZOID_DEVICE_SERIAL_NUMBER"></a><dl>
<dt><b>szOID_DEVICE_SERIAL_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
Printable string.
Labeling attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_DOMAIN_COMPONENT"></a><a id="szoid_domain_component"></a><a id="SZOID_DOMAIN_COMPONENT"></a><dl>
<dt><b>szOID_DOMAIN_COMPONENT</b></dt>
</dl>
</td>
<td width="60%">
IA5 string. DNS name component such as "com."

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_FACSIMILE_TELEPHONE_NUMBER"></a><a id="szoid_facsimile_telephone_number"></a><a id="SZOID_FACSIMILE_TELEPHONE_NUMBER"></a><dl>
<dt><b>szOID_FACSIMILE_TELEPHONE_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
Telecommunications addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_GIVEN_NAME"></a><a id="szoid_given_name"></a><a id="SZOID_GIVEN_NAME"></a><dl>
<dt><b>szOID_GIVEN_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Name attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_INITIALS"></a><a id="szoid_initials"></a><a id="SZOID_INITIALS"></a><dl>
<dt><b>szOID_INITIALS</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string. Name attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_INTERNATIONAL_ISDN_NUMBER"></a><a id="szoid_international_isdn_number"></a><a id="SZOID_INTERNATIONAL_ISDN_NUMBER"></a><dl>
<dt><b>szOID_INTERNATIONAL_ISDN_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
Numeric string.
Telecommunications addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_LOCALITY_NAME"></a><a id="szoid_locality_name"></a><a id="SZOID_LOCALITY_NAME"></a><dl>
<dt><b>szOID_LOCALITY_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Geographic attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_MEMBER"></a><a id="szoid_member"></a><a id="SZOID_MEMBER"></a><dl>
<dt><b>szOID_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
Relational application attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_ORGANIZATION_NAME"></a><a id="szoid_organization_name"></a><a id="SZOID_ORGANIZATION_NAME"></a><dl>
<dt><b>szOID_ORGANIZATION_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Organizational attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_ORGANIZATIONAL_UNIT_NAME"></a><a id="szoid_organizational_unit_name"></a><a id="SZOID_ORGANIZATIONAL_UNIT_NAME"></a><dl>
<dt><b>szOID_ORGANIZATIONAL_UNIT_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Organizational attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_OWNER"></a><a id="szoid_owner"></a><a id="SZOID_OWNER"></a><dl>
<dt><b>szOID_OWNER</b></dt>
</dl>
</td>
<td width="60%">
Relational application attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_PHYSICAL_DELIVERY_OFFICE_NAME"></a><a id="szoid_physical_delivery_office_name"></a><a id="SZOID_PHYSICAL_DELIVERY_OFFICE_NAME"></a><dl>
<dt><b>szOID_PHYSICAL_DELIVERY_OFFICE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Postal addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_PKCS_12_FRIENDLY_NAME_ATTR"></a><a id="szoid_pkcs_12_friendly_name_attr"></a><a id="SZOID_PKCS_12_FRIENDLY_NAME_ATTR"></a><dl>
<dt><b>szOID_PKCS_12_FRIENDLY_NAME_ATTR</b></dt>
</dl>
</td>
<td width="60%">
PKCS #12 attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_PKCS_12_LOCAL_KEY_ID"></a><a id="szoid_pkcs_12_local_key_id"></a><a id="SZOID_PKCS_12_LOCAL_KEY_ID"></a><dl>
<dt><b>szOID_PKCS_12_LOCAL_KEY_ID</b></dt>
</dl>
</td>
<td width="60%">
PKCS #12 attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_POST_OFFICE_BOX"></a><a id="szoid_post_office_box"></a><a id="SZOID_POST_OFFICE_BOX"></a><dl>
<dt><b>szOID_POST_OFFICE_BOX</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Postal addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_POSTAL_ADDRESS"></a><a id="szoid_postal_address"></a><a id="SZOID_POSTAL_ADDRESS"></a><dl>
<dt><b>szOID_POSTAL_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Printable string.
Postal addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_POSTAL_CODE"></a><a id="szoid_postal_code"></a><a id="SZOID_POSTAL_CODE"></a><dl>
<dt><b>szOID_POSTAL_CODE</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Postal addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_PREFERRED_DELIVERY_METHOD"></a><a id="szoid_preferred_delivery_method"></a><a id="SZOID_PREFERRED_DELIVERY_METHOD"></a><dl>
<dt><b>szOID_PREFERRED_DELIVERY_METHOD</b></dt>
</dl>
</td>
<td width="60%">
Preference attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_PRESENTATION_ADDRESS"></a><a id="szoid_presentation_address"></a><a id="SZOID_PRESENTATION_ADDRESS"></a><dl>
<dt><b>szOID_PRESENTATION_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
OSI application attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_REGISTERED_ADDRESS"></a><a id="szoid_registered_address"></a><a id="SZOID_REGISTERED_ADDRESS"></a><dl>
<dt><b>szOID_REGISTERED_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Telecommunications addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_ROLE_OCCUPANT"></a><a id="szoid_role_occupant"></a><a id="SZOID_ROLE_OCCUPANT"></a><dl>
<dt><b>szOID_ROLE_OCCUPANT</b></dt>
</dl>
</td>
<td width="60%">
Relational application attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_RSA_emailAddr"></a><a id="szoid_rsa_emailaddr"></a><a id="SZOID_RSA_EMAILADDR"></a><dl>
<dt><b>szOID_RSA_emailAddr</b></dt>
</dl>
</td>
<td width="60%">
IA5 string.
Email attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_SEARCH_GUIDE"></a><a id="szoid_search_guide"></a><a id="SZOID_SEARCH_GUIDE"></a><dl>
<dt><b>szOID_SEARCH_GUIDE</b></dt>
</dl>
</td>
<td width="60%">
Explanatory attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_SEE_ALSO"></a><a id="szoid_see_also"></a><a id="SZOID_SEE_ALSO"></a><dl>
<dt><b>szOID_SEE_ALSO</b></dt>
</dl>
</td>
<td width="60%">
Relational application attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_STATE_OR_PROVINCE_NAME"></a><a id="szoid_state_or_province_name"></a><a id="SZOID_STATE_OR_PROVINCE_NAME"></a><dl>
<dt><b>szOID_STATE_OR_PROVINCE_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Geographic attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_STREET_ADDRESS"></a><a id="szoid_street_address"></a><a id="SZOID_STREET_ADDRESS"></a><dl>
<dt><b>szOID_STREET_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Geographic attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_SUPPORTED_APPLICATION_CONTEXT"></a><a id="szoid_supported_application_context"></a><a id="SZOID_SUPPORTED_APPLICATION_CONTEXT"></a><dl>
<dt><b>szOID_SUPPORTED_APPLICATION_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
OSI application attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_SUR_NAME"></a><a id="szoid_sur_name"></a><a id="SZOID_SUR_NAME"></a><dl>
<dt><b>szOID_SUR_NAME</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Labeling attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_TELEPHONE_NUMBER"></a><a id="szoid_telephone_number"></a><a id="SZOID_TELEPHONE_NUMBER"></a><dl>
<dt><b>szOID_TELEPHONE_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
Telecommunications addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_TELETEXT_TERMINAL_IDENTIFIER"></a><a id="szoid_teletext_terminal_identifier"></a><a id="SZOID_TELETEXT_TERMINAL_IDENTIFIER"></a><dl>
<dt><b>szOID_TELETEXT_TERMINAL_IDENTIFIER</b></dt>
</dl>
</td>
<td width="60%">
Telecommunications addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_TELEX_NUMBER"></a><a id="szoid_telex_number"></a><a id="SZOID_TELEX_NUMBER"></a><dl>
<dt><b>szOID_TELEX_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
Telecommunications addressing attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_TITLE"></a><a id="szoid_title"></a><a id="SZOID_TITLE"></a><dl>
<dt><b>szOID_TITLE</b></dt>
</dl>
</td>
<td width="60%">
Case-insensitive string.
Organizational attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_USER_CERTIFICATE"></a><a id="szoid_user_certificate"></a><a id="SZOID_USER_CERTIFICATE"></a><dl>
<dt><b>szOID_USER_CERTIFICATE</b></dt>
</dl>
</td>
<td width="60%">
Security attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_USER_PASSWORD"></a><a id="szoid_user_password"></a><a id="SZOID_USER_PASSWORD"></a><dl>
<dt><b>szOID_USER_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
Security attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_X21_ADDRESS"></a><a id="szoid_x21_address"></a><a id="SZOID_X21_ADDRESS"></a><dl>
<dt><b>szOID_X21_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Numeric string.
Telecommunications addressing attribute.

</td>
</tr>
</table>

### -field dwValueType

Indicates the interpretation of the <b>Value</b> member. 




This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ANY_TYPE"></a><a id="cert_rdn_any_type"></a><dl>
<dt><b>CERT_RDN_ANY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszObjId</b> member determines the assumed type and length.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_BMP_STRING"></a><a id="cert_rdn_bmp_string"></a><dl>
<dt><b>CERT_RDN_BMP_STRING</b></dt>
</dl>
</td>
<td width="60%">
An array of Unicode characters (16-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ENCODED_BLOB"></a><a id="cert_rdn_encoded_blob"></a><dl>
<dt><b>CERT_RDN_ENCODED_BLOB</b></dt>
</dl>
</td>
<td width="60%">
An encoded data BLOB.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_GENERAL_STRING"></a><a id="cert_rdn_general_string"></a><dl>
<dt><b>CERT_RDN_GENERAL_STRING</b></dt>
</dl>
</td>
<td width="60%">
Currently not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_GRAPHIC_STRING"></a><a id="cert_rdn_graphic_string"></a><dl>
<dt><b>CERT_RDN_GRAPHIC_STRING</b></dt>
</dl>
</td>
<td width="60%">
Currently not used.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_IA5_STRING"></a><a id="cert_rdn_ia5_string"></a><dl>
<dt><b>CERT_RDN_IA5_STRING</b></dt>
</dl>
</td>
<td width="60%">
An arbitrary string of IA5 (<a href="/windows/desktop/SecGloss/a-gly">ASCII</a>) characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_INT4_STRING"></a><a id="cert_rdn_int4_string"></a><dl>
<dt><b>CERT_RDN_INT4_STRING</b></dt>
</dl>
</td>
<td width="60%">
An array of <b>INT4</b> elements (32-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ISO646_STRING"></a><a id="cert_rdn_iso646_string"></a><dl>
<dt><b>CERT_RDN_ISO646_STRING</b></dt>
</dl>
</td>
<td width="60%">
A 128-character set (8-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_NUMERIC_STRING"></a><a id="cert_rdn_numeric_string"></a><dl>
<dt><b>CERT_RDN_NUMERIC_STRING</b></dt>
</dl>
</td>
<td width="60%">
Only the characters 0 through 9 and the space character (8-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_OCTET_STRING"></a><a id="cert_rdn_octet_string"></a><dl>
<dt><b>CERT_RDN_OCTET_STRING</b></dt>
</dl>
</td>
<td width="60%">
An arbitrary string of octets (8-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_PRINTABLE_STRING"></a><a id="cert_rdn_printable_string"></a><dl>
<dt><b>CERT_RDN_PRINTABLE_STRING</b></dt>
</dl>
</td>
<td width="60%">
An arbitrary string of printable characters (8-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_T61_STRING"></a><a id="cert_rdn_t61_string"></a><dl>
<dt><b>CERT_RDN_T61_STRING</b></dt>
</dl>
</td>
<td width="60%">
An arbitrary string of T.61 characters (8-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_TELETEX_STRING"></a><a id="cert_rdn_teletex_string"></a><dl>
<dt><b>CERT_RDN_TELETEX_STRING</b></dt>
</dl>
</td>
<td width="60%">
An arbitrary string of T.61 characters (8-bit)

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_UNICODE_STRING"></a><a id="cert_rdn_unicode_string"></a><dl>
<dt><b>CERT_RDN_UNICODE_STRING</b></dt>
</dl>
</td>
<td width="60%">
An array of Unicode characters (16-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_UNIVERSAL_STRING"></a><a id="cert_rdn_universal_string"></a><dl>
<dt><b>CERT_RDN_UNIVERSAL_STRING</b></dt>
</dl>
</td>
<td width="60%">
An array of <b>INT4</b> elements (32-bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_UTF8_STRING"></a><a id="cert_rdn_utf8_string"></a><dl>
<dt><b>CERT_RDN_UTF8_STRING</b></dt>
</dl>
</td>
<td width="60%">
An array of 16 bit Unicode characters UTF8 encoded on the wire as a sequence of one, two, or three, eight-bit characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_VIDEOTEX_STRING"></a><a id="cert_rdn_videotex_string"></a><dl>
<dt><b>CERT_RDN_VIDEOTEX_STRING</b></dt>
</dl>
</td>
<td width="60%">
An arbitrary string of videotext characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_VISIBLE_STRING"></a><a id="cert_rdn_visible_string"></a><dl>
<dt><b>CERT_RDN_VISIBLE_STRING</b></dt>
</dl>
</td>
<td width="60%">
A 95-character set (8-bit).

</td>
</tr>
</table>
 


The following flags can be combined by using a bitwise-<b>OR</b> operation into the <b>dwValueType</b> member.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_DISABLE_CHECK_TYPE_FLAG"></a><a id="cert_rdn_disable_check_type_flag"></a><dl>
<dt><b>CERT_RDN_DISABLE_CHECK_TYPE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
For encoding. When set, the characters are not checked to determine whether they are valid for the value type.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_DISABLE_IE4_UTF8_FLAG"></a><a id="cert_rdn_disable_ie4_utf8_flag"></a><dl>
<dt><b>CERT_RDN_DISABLE_IE4_UTF8_FLAG</b></dt>
</dl>
</td>
<td width="60%">
For decoding. By default, <b>CERT_RDN_T61_STRING</b> encoded values are initially decoded as UTF8. If the UTF8 decoding fails, the value is decoded as 8-bit characters. If this flag is set, it skips the initial attempt to decode as UTF8 and decodes the value as 8-bit characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ENABLE_T61_UNICODE_FLAG"></a><a id="cert_rdn_enable_t61_unicode_flag"></a><dl>
<dt><b>CERT_RDN_ENABLE_T61_UNICODE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
For encoding. When set, if all the Unicode characters are &lt;= 0xFF, the <b>CERT_RDN_T61_STRING</b> value is selected instead of the <b>CERT_RDN_UNICODE_STRING</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ENABLE_UTF8_UNICODE_FLAG"></a><a id="cert_rdn_enable_utf8_unicode_flag"></a><dl>
<dt><b>CERT_RDN_ENABLE_UTF8_UNICODE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
For encoding. When set, strings are encoded with the <b>CERT_RDN_UTF8_STRING</b> value instead of
the <b>CERT_RDN_UNICODE_STRING</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_FORCE_UTF8_UNICODE_FLAG"></a><a id="cert_rdn_force_utf8_unicode_flag"></a><dl>
<dt><b>CERT_RDN_FORCE_UTF8_UNICODE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
For encoding. When set, strings are encoded with the <b>CERT_RDN_UTF8_STRING</b> value instead of <b>CERT_RDN_PRINTABLE_STRING</b> value for DirectoryString types. In addition, <b>CERT_RDN_ENABLE_UTF8_UNICODE_FLAG</b> is enabled.


<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ENABLE_PUNYCODE_FLAG"></a><a id="cert_rdn_enable_punycode_flag"></a><dl>
<dt><b>CERT_RDN_ENABLE_PUNYCODE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
For encoding.  If the string contains an email RDN, and the email address is Punycode encoded, then the resultant email address is encoded as an <b>IA5String</b>. The Punycode encoding of the host name is performed on
a label-by-label basis.


For decoding. If the name contains an email RDN, and the local part or host name
 portion of the email address contains a Punycode encoded <b>IA5String</b>,
the RDN string value is converted to its Unicode equivalent.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
</table>

### -field Value

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_RDN_VALUE_BLOB</a> that contains the attribute value. The <b>cbData</b> member of <b>Value</b> is the length, in bytes, of the <b>pbData</b> member. It is not the number of elements in the <b>pbData</b> string. 




For example, a <b>DWORD</b> is 32 bits or 4 bytes long. If <b>pbData</b> is a <b>DWORD</b> array, <b>cbData</b> would be four times the number of <b>DWORD</b> elements in the array. A <b>SHORT</b> is 16 bits or 2 bytes long. If <b>pbData</b> is an array of <b>SHORT</b> elements, <b>cbData</b> must be two times the length of the array.

The <b>pbData</b> member of <b>Value</b> can be a null-terminated array of 8-bit or 16-bit characters or a fixed-length array of elements. If <b>dwValueType</b> is set to CERT_RDN_ENCODED_BLOB, <b>pbData</b> is encoded.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certisrdnattrsincertificatename">CertIsRDNAttrsInCertificateName</a>
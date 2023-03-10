---
UID: NE:certenroll.ObjectIdGroupId
title: ObjectIdGroupId (certenroll.h)
description: Specifies the category or group to which an object identifier (OID) belongs.
helpviewer_keywords: ["ObjectIdGroupId","ObjectIdGroupId enumeration [Security]","XCN_CRYPT_ANY_GROUP_ID","XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID","XCN_CRYPT_ENHKEY_USAGE_OID_GROUP_ID","XCN_CRYPT_EXT_OR_ATTR_OID_GROUP_ID","XCN_CRYPT_FIRST_ALG_OID_GROUP_ID","XCN_CRYPT_HASH_ALG_OID_GROUP_ID","XCN_CRYPT_KEY_LENGTH_MASK","XCN_CRYPT_LAST_ALG_OID_GROUP_ID","XCN_CRYPT_LAST_OID_GROUP_ID","XCN_CRYPT_OID_DISABLE_SEARCH_DS_FLAG","XCN_CRYPT_POLICY_OID_GROUP_ID","XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID","XCN_CRYPT_RDN_ATTR_OID_GROUP_ID","XCN_CRYPT_SIGN_ALG_OID_GROUP_ID","XCN_CRYPT_TEMPLATE_OID_GROUP_ID","certenroll/ObjectIdGroupId","certenroll/XCN_CRYPT_ANY_GROUP_ID","certenroll/XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID","certenroll/XCN_CRYPT_ENHKEY_USAGE_OID_GROUP_ID","certenroll/XCN_CRYPT_EXT_OR_ATTR_OID_GROUP_ID","certenroll/XCN_CRYPT_FIRST_ALG_OID_GROUP_ID","certenroll/XCN_CRYPT_HASH_ALG_OID_GROUP_ID","certenroll/XCN_CRYPT_KEY_LENGTH_MASK","certenroll/XCN_CRYPT_LAST_ALG_OID_GROUP_ID","certenroll/XCN_CRYPT_LAST_OID_GROUP_ID","certenroll/XCN_CRYPT_OID_DISABLE_SEARCH_DS_FLAG","certenroll/XCN_CRYPT_POLICY_OID_GROUP_ID","certenroll/XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID","certenroll/XCN_CRYPT_RDN_ATTR_OID_GROUP_ID","certenroll/XCN_CRYPT_SIGN_ALG_OID_GROUP_ID","certenroll/XCN_CRYPT_TEMPLATE_OID_GROUP_ID","security.objectidgroupid_enum"]
old-location: security\objectidgroupid_enum.htm
tech.root: security
ms.assetid: 66a70cad-ce72-461b-8d71-605a62dd35b4
ms.date: 12/05/2018
ms.keywords: ObjectIdGroupId, ObjectIdGroupId enumeration [Security], XCN_CRYPT_ANY_GROUP_ID, XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID, XCN_CRYPT_ENHKEY_USAGE_OID_GROUP_ID, XCN_CRYPT_EXT_OR_ATTR_OID_GROUP_ID, XCN_CRYPT_FIRST_ALG_OID_GROUP_ID, XCN_CRYPT_HASH_ALG_OID_GROUP_ID, XCN_CRYPT_KEY_LENGTH_MASK, XCN_CRYPT_LAST_ALG_OID_GROUP_ID, XCN_CRYPT_LAST_OID_GROUP_ID, XCN_CRYPT_OID_DISABLE_SEARCH_DS_FLAG, XCN_CRYPT_POLICY_OID_GROUP_ID, XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID, XCN_CRYPT_RDN_ATTR_OID_GROUP_ID, XCN_CRYPT_SIGN_ALG_OID_GROUP_ID, XCN_CRYPT_TEMPLATE_OID_GROUP_ID, certenroll/ObjectIdGroupId, certenroll/XCN_CRYPT_ANY_GROUP_ID, certenroll/XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID, certenroll/XCN_CRYPT_ENHKEY_USAGE_OID_GROUP_ID, certenroll/XCN_CRYPT_EXT_OR_ATTR_OID_GROUP_ID, certenroll/XCN_CRYPT_FIRST_ALG_OID_GROUP_ID, certenroll/XCN_CRYPT_HASH_ALG_OID_GROUP_ID, certenroll/XCN_CRYPT_KEY_LENGTH_MASK, certenroll/XCN_CRYPT_LAST_ALG_OID_GROUP_ID, certenroll/XCN_CRYPT_LAST_OID_GROUP_ID, certenroll/XCN_CRYPT_OID_DISABLE_SEARCH_DS_FLAG, certenroll/XCN_CRYPT_POLICY_OID_GROUP_ID, certenroll/XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID, certenroll/XCN_CRYPT_RDN_ATTR_OID_GROUP_ID, certenroll/XCN_CRYPT_SIGN_ALG_OID_GROUP_ID, certenroll/XCN_CRYPT_TEMPLATE_OID_GROUP_ID, security.objectidgroupid_enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ObjectIdGroupId
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ObjectIdGroupId
 - certenroll/ObjectIdGroupId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - ObjectIdGroupId
---

# ObjectIdGroupId enumeration


## -description

The <b>ObjectIdGroupId</b> enumeration type specifies the category or group to which an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) belongs. This enumeration is used when calling <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a> to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object.

## -enum-fields

### -field XCN_CRYPT_ANY_GROUP_ID:0

The group OID is not identified. All OID groups will be included when searching.

### -field XCN_CRYPT_HASH_ALG_OID_GROUP_ID:1

Hashing algorithm group. This includes the following OIDs:<ul>
<li>XCN_OID_OIWSEC_sha (1.3.14.3.2.18)</li>
<li>XCN_OID_OIWSEC_sha1 (1.3.14.3.2.26)</li>
<li>XCN_OID_RSA_MD2 (1.2.840.113549.2.2)</li>
<li>XCN_OID_RSA_MD4 (1.2.840.113549.2.4)</li>
<li>XCN_OID_RSA_MD5 (1.2.840.113549.2.5)</li>
</ul>

### -field XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID:2

Symmetric encryption algorithm group. This includes the following OIDs:<ul>
<li>XCN_OID_NIST_AES128_CBC (2.16.840.1.101.3.4.1.2)</li>
<li>XCN_OID_NIST_AES192_CBC (2.16.840.1.101.3.4.1.22)</li>
<li>XCN_OID_NIST_AES256_CBC (2.16.840.1.101.3.4.1.42)</li>
<li>XCN_OID_NIST_AES128_WRAP (2.16.840.1.101.3.4.1.5)</li>
<li>XCN_OID_NIST_AES192_WRAP (2.16.840.1.101.3.4.1.25)</li>
<li>XCN_OID_NIST_AES256_WRAP (2.16.840.1.101.3.4.1.45)</li>
<li>XCN_OID_OIWSEC_desCBC (1.3.14.3.2.7)</li>
<li>XCN_OID_RSA_DES_EDE3_CBC (1.2.840.113549.3.7)</li>
<li>XCN_OID_RSA_RC2CBC (1.2.840.113549.3.2)</li>
<li>XCN_OID_RSA_RC4 (1.2.840.113549.3.4)</li>
<li>XCN_OID_RSA_SMIMEalgCMS3DESwrap (1.2.840.113549.1.9.16.3.6)</li>
<li>XCN_OID_RSA_SMIMEalgCMSRC2wrap (1.2.840.113549.1.9.16.3.7)</li>
</ul>

### -field XCN_CRYPT_PUBKEY_ALG_OID_GROUP_ID:3

Asymmetric encryption algorithm group. This includes the following OIDs:<ul>
<li>XCN_OID_ANSI_X942_DH (1.2.840.10046.2.1)</li>
<li>XCN_OID_DH_SINGLE_PASS_STDDH_SHA1_KDF (1.3.133.16.840.63.0.2)</li>
<li>XCN_OID_ECC_CURVE_P256 (1.2.840.10045.3.1.7)</li>
<li>XCN_OID_ECC_CURVE_P384 (1.3.132.0.34)</li>
<li>XCN_OID_ECC_CURVE_P521 (1.3.132.0.35)</li>
<li>XCN_OID_ECC_PUBLIC_KEY (1.2.840.10045.2.1)</li>
<li>XCN_OID_INFOSEC_mosaicKMandUpdSig (2.16.840.1.101.2.1.1.20)</li>
<li>XCN_OID_OIWSEC_dsa (1.3.14.3.2.12)</li>
<li>XCN_OID_OIWSEC_rsaXchg (1.3.14.3.2.22)</li>
<li>XCN_OID_PKIX_NO_SIGNATURE (1.3.6.1.5.5.7.6.2)</li>
<li>XCN_OID_RSA_DH (1.2.840.113549.1.3.1)</li>
<li>XCN_OID_RSA_RSA (1.2.840.113549.1.1.1)</li>
<li>XCN_OID_RSA_SMIMEalgESDH (1.2.840.113549.1.9.16.3.5)</li>
<li>XCN_OID_RSAES_OAEP (1.2.840.113549.1.1.7)</li>
<li>XCN_OID_X957_DSA (1.2.840.10040.4.1)</li>
</ul>

### -field XCN_CRYPT_SIGN_ALG_OID_GROUP_ID:4

Signing algorithm group. This includes the following OIDs:<ul>
<li>XCN_OID_ECDSA_SHA1 (1.2.840.10045.4.1)</li>
<li>XCN_OID_ECDSA_SHA256 (1.2.840.10045.4.3.2)</li>
<li>XCN_OID_ECDSA_SHA384 (1.2.840.10045.4.3.3)</li>
<li>XCN_OID_ECDSA_SHA512 (1.2.840.10045.4.3.4)</li>
<li>XCN_OID_ECDSA_SPECIFIED (1.2.840.10045.4.3)</li>
<li>XCN_OID_INFOSEC_mosaicUpdatedSig (2.16.840.1.101.2.1.1.19)</li>
<li>XCN_OID_NIST_sha256 (2.16.840.1.101.3.4.2.1)</li>
<li>XCN_OID_NIST_sha384 (2.16.840.1.101.3.4.2.2)</li>
<li>XCN_OID_NIST_sha512 (2.16.840.1.101.3.4.2.3)</li>
<li>XCN_OID_OIWDIR_md2RSA (1.3.14.7.2.3.1)</li>
<li>XCN_OID_OIWSEC_dsaSHA1 (1.3.14.3.2.27)</li>
<li>XCN_OID_OIWSEC_md4RSA (1.3.14.3.2.2)</li>
<li>XCN_OID_OIWSEC_md4RSA2 (1.3.14.3.2.4)</li>
<li>XCN_OID_OIWSEC_md5RSA (1.3.14.3.2.3)</li>
<li>XCN_OID_OIWSEC_sha1 (1.3.14.3.2.26)</li>
<li>XCN_OID_OIWSEC_sha1RSASign (1.3.14.3.2.29)</li>
<li>XCN_OID_OIWSEC_shaDSA (1.3.14.3.2.13)</li>
<li>XCN_OID_OIWSEC_shaRSA (1.3.14.3.2.15)</li>
<li>XCN_OID_RSA_MD2RSA (1.2.840.113549.1.1.2)</li>
<li>XCN_OID_RSA_MD4RSA (1.2.840.113549.1.1.3)</li>
<li>XCN_OID_RSA_MD5 (1.2.840.113549.2.5)</li>
<li>XCN_OID_RSA_MD5RSA (1.2.840.113549.1.1.4)</li>
<li>XCN_OID_RSA_SHA1RSA (1.2.840.113549.1.1.5)</li>
<li>XCN_OID_RSA_SHA256RSA (1.2.840.113549.1.1.11)</li>
<li>XCN_OID_RSA_SHA384RSA (1.2.840.113549.1.1.12)</li>
<li>XCN_OID_RSA_SHA512RSA (1.2.840.113549.1.1.13)</li>
<li>XCN_OID_RSA_SSA_PSS (1.2.840.113549.1.1.10)</li>
<li>XCN_OID_X957_SHA1DSA (1.2.840.10040.4.3)</li>
</ul>

### -field XCN_CRYPT_RDN_ATTR_OID_GROUP_ID:5

Relative distinguished name (RDN) group. This includes the following OIDs:<ul>
<li>XCN_OID_COMMON_NAME (2.5.4.3)</li>
<li>XCN_OID_LOCALITY_NAME (2.5.4.7)</li>
<li>XCN_OID_ORGANIZATION_NAME (2.5.4.10)</li>
<li>XCN_OID_ORGANIZATIONAL_UNIT_NAME (2.5.4.11)</li>
<li>XCN_OID_RSA_emailAddr (1.2.840.113549.1.9.1)</li>
<li>XCN_OID_COUNTRY_NAME (2.5.4.6)</li>
<li>XCN_OID_STATE_OR_PROVINCE_NAME (2.5.4.8)</li>
<li>XCN_OID_STREET_ADDRESS (2.5.4.9)</li>
<li>XCN_OID_TITLE (2.5.4.12)</li>
<li>XCN_OID_GIVEN_NAME (2.5.4.42)</li>
<li>XCN_OID_INITIALS (2.5.4.43)</li>
<li>XCN_OID_SUR_NAME (2.5.4.4)</li>
<li>XCN_OID_DEVICE_SERIAL_NUMBER (2.5.4.5)</li>
<li>XCN_OID_DOMAIN_COMPONENT (0.9.2342.19200300.100.1.25)</li>
<li>XCN_OID_DESCRIPTION (2.5.4.13)</li>
<li>XCN_OID_POSTAL_CODE (2.5.4.17)</li>
<li>XCN_OID_POST_OFFICE_BOX (2.5.4.18)</li>
<li>XCN_OID_TELEPHONE_NUMBER (2.5.4.20)</li>
<li>XCN_OID_X21_ADDRESS (2.5.4.24)</li>
<li>XCN_OID_DN_QUALIFIER (2.5.4.46)</li>
</ul>

### -field XCN_CRYPT_EXT_OR_ATTR_OID_GROUP_ID:6

Extension and attribute group. This includes the following OIDs:<ul>
<li>XCN_OID_CTL (1.3.6.1.4.1.311.10.1)</li>
<li>XCN_OID_CMC_ADD_ATTRIBUTES (1.3.6.1.4.1.311.10.10.1)</li>
<li>XCN_OID_NEXT_UPDATE_LOCATION (1.3.6.1.4.1.311.10.2)</li>
<li>XCN_OID_SERIALIZED (1.3.6.1.4.1.311.10.3.3.1)</li>
<li>XCN_OID_YESNO_TRUST_ATTR (1.3.6.1.4.1.311.10.4.1)</li>
<li>XCN_OID_CROSS_CERT_DIST_POINTS (1.3.6.1.4.1.311.10.9.1)</li>
<li>XCN_OID_ENROLLMENT_NAME_VALUE_PAIR (1.3.6.1.4.1.311.13.2.1)</li>
<li>XCN_OID_ENROLLMENT_CSP_PROVIDER (1.3.6.1.4.1.311.13.2.2)</li>
<li>XCN_OID_OS_VERSION (1.3.6.1.4.1.311.13.2.3)</li>
<li>XCN_OID_CERT_EXTENSIONS (1.3.6.1.4.1.311.2.1.14)</li>
<li>XCN_OID_ENROLL_CERTTYPE_EXTENSION (1.3.6.1.4.1.311.20.2)</li>
<li>XCN_OID_NT_PRINCIPAL_NAME (1.3.6.1.4.1.311.20.2.3)</li>
<li>XCN_OID_CERT_MANIFOLD (1.3.6.1.4.1.311.20.3)</li>
<li>XCN_OID_CERTSRV_CA_VERSION (1.3.6.1.4.1.311.21.1)</li>
<li>XCN_OID_APPLICATION_CERT_POLICIES (1.3.6.1.4.1.311.21.10)</li>
<li>XCN_OID_APPLICATION_POLICY_MAPPINGS (1.3.6.1.4.1.311.21.11)</li>
<li>XCN_OID_APPLICATION_POLICY_CONSTRAINTS (1.3.6.1.4.1.311.21.12)</li>
<li>XCN_OID_ARCHIVED_KEY_ATTR (1.3.6.1.4.1.311.21.13)</li>
<li>XCN_OID_CRL_SELF_CDP (1.3.6.1.4.1.311.21.14)</li>
<li>XCN_OID_REQUIRE_CERT_CHAIN_POLICY (1.3.6.1.4.1.311.21.15)</li>
<li>XCN_OID_ARCHIVED_KEY_CERT_HASH (1.3.6.1.4.1.311.21.16)</li>
<li>XCN_OID_CERTSRV_PREVIOUS_CERT_HASH (1.3.6.1.4.1.311.21.2)</li>
<li>XCN_OID_REQUEST_CLIENT_INFO (1.3.6.1.4.1.311.21.20)</li>
<li>XCN_OID_CERTSRV_CROSSCA_VERSION (1.3.6.1.4.1.311.21.22)</li>
<li>XCN_OID_CRL_VIRTUAL_BASE (1.3.6.1.4.1.311.21.3)</li>
<li>XCN_OID_CRL_NEXT_PUBLISH (1.3.6.1.4.1.311.21.4)</li>
<li>XCN_OID_KP_CA_EXCHANGE (1.3.6.1.4.1.311.21.5)</li>
<li>XCN_OID_KP_KEY_RECOVERY_AGENT (1.3.6.1.4.1.311.21.6)</li>
<li>XCN_OID_KP_KEY_RECOVERY_AGENT (1.3.6.1.4.1.311.21.7)</li>
<li>XCN_OID_ENTERPRISE_OID_ROOT (1.3.6.1.4.1.311.21.8)</li>
<li>XCN_OID_RDN_DUMMY_SIGNER (1.3.6.1.4.1.311.21.9)</li>
<li>XCN_OID_PRODUCT_UPDATE (1.3.6.1.4.1.311.31.1)</li>
<li>XCN_OID_AUTHORITY_INFO_ACCESS (1.3.6.1.5.5.7.1.1)</li>
<li>XCN_OID_LOGOTYPE_EXT (1.3.6.1.5.5.7.1.12)</li>
<li>XCN_OID_BIOMETRIC_EXT (1.3.6.1.5.5.7.1.2)</li>
<li>XCN_OID_CT_PKI_DATA (1.3.6.1.5.5.7.12.2)</li>
<li>XCN_OID_CT_PKI_RESPONSE (1.3.6.1.5.5.7.12.3)</li>
<li>XCN_OID_PKIX_POLICY_QUALIFIER_CPS (1.3.6.1.5.5.7.2.1)</li>
<li>XCN_OID_PKIX_POLICY_QUALIFIER_USERNOTICE (1.3.6.1.5.5.7.2.2)</li>
<li>XCN_OID_PKIX_OCSP (1.3.6.1.5.5.7.48.1)</li>
<li>XCN_OID_PKIX_OCSP_NOCHECK (1.3.6.1.5.5.7.48.1.5)</li>
<li>XCN_OID_PKIX_CA_ISSUERS (1.3.6.1.5.5.7.48.2)</li>
<li>XCN_OID_CMC (1.3.6.1.5.5.7.7)</li>
<li>XCN_OID_CMC_STATUS_INFO (1.3.6.1.5.5.7.7.1)</li>
<li>XCN_OID_CMC_GET_CERT (1.3.6.1.5.5.7.7.15)</li>
<li>XCN_OID_CMC_GET_CRL (1.3.6.1.5.5.7.7.16)</li>
<li>XCN_OID_CMC_REVOKE_REQUEST (1.3.6.1.5.5.7.7.17)</li>
<li>XCN_OID_CMC_REG_INFO (1.3.6.1.5.5.7.7.18)</li>
<li>XCN_OID_CMC_QUERY_PENDING (1.3.6.1.5.5.7.7.21)</li>
<li>XCN_OID_CMC_TRANSACTION_ID (1.3.6.1.5.5.7.7.5)</li>
<li>XCN_OID_CMC_SENDER_NONCE (1.3.6.1.5.5.7.7.6)</li>
<li>XCN_OID_CMC_RECIPIENT_NONCE (1.3.6.1.5.5.7.7.7)</li>
<li>XCN_OID_CMC_ADD_EXTENSIONS (1.3.6.1.5.5.7.7.8)</li>
<li>XCN_OID_AUTHORITY_KEY_IDENTIFIER (2.5.29.1)</li>
<li>XCN_OID_BASIC_CONSTRAINTS (2.5.29.10)</li>
<li>XCN_OID_SUBJECT_KEY_IDENTIFIER (2.5.29.14)</li>
<li>XCN_OID_KEY_USAGE (2.5.29.15)</li>
<li>XCN_OID_PRIVATEKEY_USAGE_PERIOD (2.5.29.16)</li>
<li>XCN_OID_SUBJECT_ALT_NAME2 (2.5.29.17)</li>
<li>XCN_OID_ISSUER_ALT_NAME2 (2.5.29.18)</li>
<li>XCN_OID_BASIC_CONSTRAINTS2 (2.5.29.19)</li>
<li>XCN_OID_KEY_ATTRIBUTES (2.5.29.2)</li>
<li>XCN_OID_CRL_NUMBER (2.5.29.20)</li>
<li>XCN_OID_CRL_REASON_CODE (2.5.29.21)</li>
<li>XCN_OID_DELTA_CRL_INDICATOR (2.5.29.27)</li>
<li>XCN_OID_ISSUING_DIST_POINT (2.5.29.28)</li>
<li>XCN_OID_NAME_CONSTRAINTS (2.5.29.30)</li>
<li>XCN_OID_CRL_DIST_POINTS (2.5.29.31)</li>
<li>XCN_OID_CERT_POLICIES (2.5.29.32)</li>
<li>XCN_OID_POLICY_MAPPINGS (2.5.29.33)</li>
<li>XCN_OID_AUTHORITY_KEY_IDENTIFIER2 (2.5.29.35)</li>
<li>XCN_OID_POLICY_CONSTRAINTS (2.5.29.36)</li>
<li>XCN_OID_ENHANCED_KEY_USAGE (2.5.29.37)</li>
<li>XCN_OID_KEY_USAGE_RESTRICTION (2.5.29.4)</li>
<li>XCN_OID_FRESHEST_CRL (2.5.29.46)</li>
<li>XCN_OID_LEGACY_POLICY_MAPPINGS (2.5.29.5)</li>
<li>XCN_OID_SUBJECT_ALT_NAME (2.5.29.7)</li>
<li>XCN_OID_ISSUER_ALT_NAME (2.5.29.8)</li>
<li>XCN_OID_ORGANIZATION_NAME (2.5.4.10)</li>
<li>XCN_OID_ORGANIZATIONAL_UNIT_NAME (2.5.4.11)</li>
<li>XCN_OID_TITLE (2.5.4.12)</li>
<li>XCN_OID_COMMON_NAME (2.5.4.3)</li>
<li>XCN_OID_SUR_NAME (2.5.4.4)</li>
<li>XCN_OID_GIVEN_NAME (2.5.4.42)</li>
<li>XCN_OID_INITIALS (2.5.4.43)</li>
<li>XCN_OID_DEVICE_SERIAL_NUMBER (2.5.4.5)</li>
<li>XCN_OID_COUNTRY_NAME (2.5.4.6)</li>
<li>XCN_OID_LOCALITY_NAME (2.5.4.7)</li>
<li>XCN_OID_STATE_OR_PROVINCE_NAME (2.5.4.8)</li>
<li>XCN_OID_STREET_ADDRESS (2.5.4.9)</li>
</ul>

### -field XCN_CRYPT_ENHKEY_USAGE_OID_GROUP_ID:7

Enhanced key usage (EKU) extension group. This includes the following OIDs:<ul>
<li>XCN_OID_PKIX_KP_SERVER_AUTH (1.3.6.1.5.5.7.3.1)</li>
<li>XCN_OID_PKIX_KP_CLIENT_AUTH (1.3.6.1.5.5.7.3.2)</li>
<li>XCN_OID_PKIX_KP_CODE_SIGNING (1.3.6.1.5.5.7.3.3)</li>
<li>XCN_OID_PKIX_KP_EMAIL_PROTECTION (1.3.6.1.5.5.7.3.4)</li>
<li>XCN_OID_PKIX_KP_TIMESTAMP_SIGNING (1.3.6.1.5.5.7.3.8)</li>
<li>XCN_OID_KP_CTL_USAGE_SIGNING (1.3.6.1.4.1.311.10.3.1)</li>
<li>XCN_OID_KP_TIME_STAMP_SIGNING (1.3.6.1.4.1.311.10.3.2)</li>
<li>XCN_OID_PKIX_KP_IPSEC_END_SYSTEM (1.3.6.1.5.5.7.3.5)</li>
<li>XCN_OID_PKIX_KP_IPSEC_TUNNEL (1.3.6.1.5.5.7.3.6)</li>
<li>XCN_OID_PKIX_KP_IPSEC_USER (1.3.6.1.5.5.7.3.7)</li>
<li>XCN_OID_KP_EFS (1.3.6.1.4.1.311.10.3.4)</li>
<li>XCN_OID_WHQL_CRYPTO (1.3.6.1.4.1.311.10.3.5)</li>
<li>XCN_OID_NT5_CRYPTO (1.3.6.1.4.1.311.10.3.6)</li>
<li>XCN_OID_OEM_WHQL_CRYPTO (1.3.6.1.4.1.311.10.3.7)</li>
<li>XCN_OID_EMBEDDED_NT_CRYPTO (1.3.6.1.4.1.311.10.3.8)</li>
<li>XCN_OID_LICENSES (1.3.6.1.4.1.311.10.6.1)</li>
<li>XCN_OID_LICENSE_SERVER (1.3.6.1.4.1.311.10.6.2)</li>
<li>XCN_OID_KP_SMARTCARD_LOGON (1.3.6.1.4.1.311.20.2.2)</li>
<li>XCN_OID_DRM (1.3.6.1.4.1.311.10.5.1)</li>
<li>XCN_OID_KP_QUALIFIED_SUBORDINATION (1.3.6.1.4.1.311.10.3.10)</li>
<li>XCN_OID_KP_KEY_RECOVERY (1.3.6.1.4.1.311.10.3.11)</li>
<li>XCN_OID_KP_DOCUMENT_SIGNING (1.3.6.1.4.1.311.10.3.12)</li>
<li>XCN_OID_IPSEC_KP_IKE_INTERMEDIATE (1.3.6.1.5.5.8.2.2)</li>
<li>XCN_OID_EFS_RECOVERY (1.3.6.1.4.1.311.10.3.4.1)</li>
<li>XCN_OID_ROOT_LIST_SIGNER (1.3.6.1.4.1.311.10.3.9)</li>
<li>XCN_OID_ANY_APPLICATION_POLICY (1.3.6.1.4.1.311.10.12.1)</li>
<li>XCN_OID_DS_EMAIL_REPLICATION (1.3.6.1.4.1.311.21.19)</li>
<li>XCN_OID_ENROLLMENT_AGENT (1.3.6.1.4.1.311.20.2.1)</li>
<li>XCN_OID_KP_KEY_RECOVERY_AGENT (1.3.6.1.4.1.311.21.6)</li>
<li>XCN_OID_KP_CA_EXCHANGE (1.3.6.1.4.1.311.21.5)</li>
<li>XCN_OID_KP_LIFETIME_SIGNING (1.3.6.1.4.1.311.10.3.13)</li>
<li>XCN_OID_PKIX_KP_OCSP_SIGNING (1.3.6.1.5.5.7.3.9)</li>
</ul>

### -field XCN_CRYPT_POLICY_OID_GROUP_ID:8

Issuance policy group. This includes the following OIDs. The <i>x.y.z</i> portion of each OID represents a randomly generated numeric sequence that is unique for each forest.<ul>
<li>XCN_OID_ANY_CERT_POLICY (2.5.29.32.0)</li>
<li>Low Assurance (1.3.6.1.4.1.311.21.8.x.y.z.1.400)</li>
<li>Medium Assurance (1.3.6.1.4.1.311.21.8.x.y.z.1.401)</li>
<li>High Assurance (1.3.6.1.4.1.311.21.8.x.y.z.1.402)</li>
</ul>

### -field XCN_CRYPT_TEMPLATE_OID_GROUP_ID:9

Certificate template group. The OIDs in this group identify the certificate templates that are available to the client, and all begin with 1.3.6.1.4.1.311.21.8. but are completed by randomly generated numeric sequences that are unique for each forest.

### -field XCN_CRYPT_KDF_OID_GROUP_ID:10

### -field XCN_CRYPT_LAST_OID_GROUP_ID:10

Equivalent to XCN_CRYPT_TEMPLATE_OID_GROUP_ID. You can use this value to iterate through the group OIDs.

### -field XCN_CRYPT_FIRST_ALG_OID_GROUP_ID:1

Equivalent to XCN_CRYPT_HASH_ALG_OID_GROUP_ID. You can use this value to iterate through the group algorithm OIDs.

### -field XCN_CRYPT_LAST_ALG_OID_GROUP_ID:4

Equivalent to XCN_CRYPT_SIGN_ALG_OID_GROUP_ID. You can use this value to iterate through the group algorithm OIDs.

### -field XCN_CRYPT_GROUP_ID_MASK:0xffff

### -field XCN_CRYPT_OID_PREFER_CNG_ALGID_FLAG:0x40000000

### -field XCN_CRYPT_OID_DISABLE_SEARCH_DS_FLAG:0x80000000

Not supported.

### -field XCN_CRYPT_OID_INFO_OID_GROUP_BIT_LEN_MASK:0xfff0000

### -field XCN_CRYPT_OID_INFO_OID_GROUP_BIT_LEN_SHIFT:16

### -field XCN_CRYPT_KEY_LENGTH_MASK:0xfff0000

Enables addition of a key length to the upper 16 bits of the XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID group ID. For example, to use the <a href="/windows/desktop/api/certenroll/nf-certenroll-iobjectid-initializefromalgorithmname">InitializeFromAlgorithmName</a> method to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectid">IObjectId</a> object from a 192-bit AES algorithm, specify "AES" for the <i>strAlgorithmName</i> parameter, shift the length left by 16, and perform a bitwise-<b>OR</b> combination on the shifted bit length and the <i>GroupId</i> value.


``` syntax
DWORD dwBitLen = 192;

ObjectIdGroupId GroupId = 
        (ObjectIdGroupId) (XCN_CRYPT_ENCRYPT_ALG_OID_GROUP_ID | 
        (XCN_CRYPT_KEY_LENGTH_MASK &amp; (dwBitLen &lt;&lt; 16)));

```


## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>

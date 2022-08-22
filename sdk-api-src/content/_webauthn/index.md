---
UID: TP:webauthn
title: WebAuthn API
ms.assetid: c1fef6bd-056f-4b82-bd0b-394099515f16
ms.date: 08/22/2022
ms.keywords: webauthn, ctap
ms.topic: conceptual
---

# WebAuthn

## -description

Overview of the WebAuthn technology, which provides Win32 apps with APIs for communicating to Windows Hello and external security keys as part of WebAuthn and CTAP specifications.

To develop with the WebAuthn API, you need these headers:

- [webauthn.h](../webauthn/index.md)

For programming guidance for this technology, see:

- [WebAuthn](https://w3c.github.io/webauthn/)

- [CTAP](https://fidoalliance.org/specs/fido-v2.0-ps-20190130/fido-client-to-authenticator-protocol-v2.0-ps-20190130.html)

The following constants are defined in the [webauthn.h](../webauthn/index.md) header file:

| Constant | Value | Description |
|--------|--------|--------|
| WEBAUTHN_API_VERSION_1<br/>WEBAUTHN_API_VERSION_2<br/>WEBAUTHN_API_VERSION_3<br/>WEBAUTHN_API_VERSION_4 | 1<br/>2<br/>3<br/>4 | API Version Information. Caller should check for [WebAuthNGetApiVersionNumber](nf-webauthn-webauthngetapiversionnumber.md) to check the presence of relevant APIs and features for their usage. |
| WEBAUTHN_API_CURRENT_VERSION | WEBAUTHN_API_VERSION_4 | The current API version. |
| WEBAUTHN_RP_ENTITY_INFORMATION_CURRENT_VERSION | 1 | The current version of the [WEBAUTHN_RP_ENTITY_INFORMATION](ns-webauthn-webauthn_rp_entity_information.md) structure. |
| WEBAUTHN_MAX_USER_ID_LENGTH | 64 | The max length, in bytes, of a user entity's ID. |
| WEBAUTHN_USER_ENTITY_INFORMATION_CURRENT_VERSION | 1 | The current version of the [WEBAUTHN_USER_ENTITY_INFORMATION](ns-webauthn-webauthn_user_entity_information.md) structure. |
| WEBAUTHN_HASH_ALGORITHM_SHA_256<br/>WEBAUTHN_HASH_ALGORITHM_SHA_384<br/>WEBAUTHN_HASH_ALGORITHM_SHA_512 | "SHA-256"<br/>"SHA-384"<br/>"SHA-512" | The hash algorithm ID used to hash the client data. |
| WEBAUTHN_CLIENT_DATA_CURRENT_VERSION | 1 | Version of the [WEBAUTHN_CLIENT_DATA](ns-webauthn-webauthn_client_data.md) structure, to allow for modifications in the future. |
| WEBAUTHN_CREDENTIAL_TYPE_PUBLIC_KEY | "public-key" | Well-known credential type specifying a credential to create. |
| WEBAUTHN_COSE_ALGORITHM_ECDSA_P256_WITH_SHA256<br/>WEBAUTHN_COSE_ALGORITHM_ECDSA_P384_WITH_SHA384<br/>WEBAUTHN_COSE_ALGORITHM_ECDSA_P521_WITH_SHA512<br/>WEBAUTHN_COSE_ALGORITHM_RSASSA_PKCS1_V1_5_WITH_SHA256<br/>WEBAUTHN_COSE_ALGORITHM_RSASSA_PKCS1_V1_5_WITH_SHA384<br/>WEBAUTHN_COSE_ALGORITHM_RSASSA_PKCS1_V1_5_WITH_SHA512<br/>WEBAUTHN_COSE_ALGORITHM_RSA_PSS_WITH_SHA256<br/>WEBAUTHN_COSE_ALGORITHM_RSA_PSS_WITH_SHA384<br/>WEBAUTHN_COSE_ALGORITHM_RSA_PSS_WITH_SHA512 | -7<br/>-35<br/>-36<br/>-257<br/>-258<br/>-259<br/>-37<br/>-38<br/>-39 | Well-known COSE algorithm specifying the algorithm to use for the credential. |
| WEBAUTHN_COSE_CREDENTIAL_PARAMETER_CURRENT_VERSION | 1 | The current version of the [WEBAUTHN_COSE_CREDENTIAL_PARAMETER](ns-webauthn-webauthn_cose_credential_parameter.md) structure, to allow for modifications in the future. |
| WEBAUTHN_CREDENTIAL_CURRENT_VERSION | 1 | The current version of the [WEBAUTHN_CREDENTIAL](ns-webauthn-webauthn_credential.md) structure, to allow for modifications in the future. |
| WEBAUTHN_CTAP_TRANSPORT_USB<br/>WEBAUTHN_CTAP_TRANSPORT_NFC<br/>WEBAUTHN_CTAP_TRANSPORT_BLE<br/>WEBAUTHN_CTAP_TRANSPORT_TEST<br/>WEBAUTHN_CTAP_TRANSPORT_INTERNAL<br/>WEBAUTHN_CTAP_TRANSPORT_FLAGS_MASK | 0x00000001<br/>0x00000002<br/>0x00000004<br/>0x00000008<br/>0x00000010<br/>0x0000001F | Credential transports. `0` implies no transport restrictions. |
| WEBAUTHN_CREDENTIAL_EX_CURRENT_VERSION | 1 | The current version of the [WEBAUTHN_CREDENTIAL_EX](ns-webauthn-webauthn_credential_ex.md) structure, to allow for modifications in the future. |
| WEBAUTHN_CREDENTIAL_DETAILS_VERSION_1 | 1 | The version of the [WEBAUTHN_CREDENTIAL_DETAILS](ns-webauthn-webauthn_credential_details.md) structure, to allow for modifications in the future. |
| WEBAUTHN_CREDENTIAL_DETAILS_CURRENT_VERSION | WEBAUTHN_CREDENTIAL_DETAILS_VERSION_1 | The current version of the [WEBAUTHN_CREDENTIAL_DETAILS](ns-webauthn-webauthn_credential_details.md) structure, to allow for modifications in the future. |
| WEBAUTHN_GET_CREDENTIALS_OPTIONS_VERSION_1 | 1 | The version of the [WEBAUTHN_GET_CREDENTIALS_OPTIONS](ns-webauthn-webauthn_get_credentials_options.md) structure, to allow for modifications in the future. |
| WEBAUTHN_GET_CREDENTIALS_OPTIONS_CURRENT_VERSION | WEBAUTHN_GET_CREDENTIALS_OPTIONS_VERSION_1 | The current version of the [WEBAUTHN_GET_CREDENTIALS_OPTIONS](ns-webauthn-webauthn_get_credentials_options.md) structure, to allow for modifications in the future. |
| WEBAUTHN_CTAP_ONE_HMAC_SECRET_LENGTH | 32 | If caller wants to provide RAW Hmac-Secret SALT values directly in [WEBAUTHN_HMAC_SECRET_SALT](./ns-webauthn-webauthn_hmac_secret_salt.md) structure, values provided must be of this size. |
| WEBAUTHN_EXTENSIONS_IDENTIFIER_HMAC_SECRET | "hmac-secret" | MakeCredential Input Type: BOOL.<ul><li>pvExtension must point to a BOOL with the value TRUE.</li><li>cbExtension must contain the sizeof(BOOL).</li></ul>MakeCredential Output Type: BOOL.<ul><li>pvExtension will point to a BOOL with the value TRUE if credential was successfully created with HMAC_SECRET.</li><li>cbExtension will contain the sizeof(BOOL).</li></ul>GetAssertion Input Type: Not Supported<br/>GetAssertion Output Type: Not Supported |
| WEBAUTHN_USER_VERIFICATION_ANY<br/>WEBAUTHN_USER_VERIFICATION_OPTIONAL<br/>WEBAUTHN_USER_VERIFICATION_OPTIONAL_WITH_CREDENTIAL_ID_LIST<br/>WEBAUTHN_USER_VERIFICATION_REQUIRED | 0<br/>1<br/>2<br/>3 | User verification option for credential protection in the [WEBAUTHN_CRED_PROTECT_EXTENSION_IN](ns-webauthn-webauthn_cred_protect_extension_in.md) structure. |
| WEBAUTHN_EXTENSIONS_IDENTIFIER_CRED_PROTECT | "credProtect" | MakeCredential Input Type: WEBAUTHN_CRED_PROTECT_EXTENSION_IN.<ul><li>pvExtension must point to a WEBAUTHN_CRED_PROTECT_EXTENSION_IN struct</li><li>cbExtension will contain the sizeof(WEBAUTHN_CRED_PROTECT_EXTENSION_IN).</li></ul>MakeCredential Output Type:  DWORD.<ul><li>pvExtension will point to a DWORD with one of the above WEBAUTHN_USER_VERIFICATION_* values if credential was successfully created with CRED_PROTECT.</li><li>cbExtension will contain the sizeof(DWORD).</li></ul>GetAssertion Input Type: Not Supported<br/>GetAssertion Output Type: Not Supported |
| WEBAUTHN_EXTENSIONS_IDENTIFIER_CRED_BLOB | "credBlob" | MakeCredential Input Type:   WEBAUTHN_CRED_BLOB_EXTENSION.<ul><li>pvExtension must point to a WEBAUTHN_CRED_BLOB_EXTENSION struct</li><li>cbExtension must contain the sizeof(WEBAUTHN_CRED_BLOB_EXTENSION).</li></ul>MakeCredential Output Type:  BOOL.<ul><li>pvExtension will point to a BOOL with the value TRUE if credBlob was successfully created</li><li>cbExtension will contain the sizeof(BOOL).</li></ul>GetAssertion Input Type: BOOL.<ul><li>pvExtension must point to a BOOL with the value TRUE to request the credBlob.</li><li>cbExtension must contain the sizeof(BOOL).</li></ul>GetAssertion Output Type: WEBAUTHN_CRED_BLOB_EXTENSION.<ul><li>pvExtension will point to a WEBAUTHN_CRED_BLOB_EXTENSION struct if the authenticator returns the credBlob in the signed extensions.</li><li>cbExtension will contain the sizeof(WEBAUTHN_CRED_BLOB_EXTENSION).</li></ul> |
| WEBAUTHN_EXTENSIONS_IDENTIFIER_MIN_PIN_LENGTH | "minPinLength" | MakeCredential Input Type: BOOL.<ul><li>pvExtension must point to a BOOL with the value TRUE to request the minPinLength.</li><li>cbExtension must contain the sizeof(BOOL).</li></ul>MakeCredential Output Type: DWORD.<ul><li>pvExtension will point to a DWORD with the minimum pin length if returned by the authenticator.</li><li>cbExtension will contain the sizeof(DWORD).</li></ul>GetAssertion Input Type: Not Supported<br/>GetAssertion Output Type: Not Supported |
| WEBAUTHN_AUTHENTICATOR_ATTACHMENT_ANY<br/>WEBAUTHN_AUTHENTICATOR_ATTACHMENT_PLATFORM<br/>WEBAUTHN_AUTHENTICATOR_ATTACHMENT_CROSS_PLATFORM<br/>WEBAUTHN_AUTHENTICATOR_ATTACHMENT_CROSS_PLATFORM_U2F_V2 | 0<br/>1<br/>2<br/>3 | Platform vs cross-platform authenticator options. |
| WEBAUTHN_USER_VERIFICATION_REQUIREMENT_ANY<br/>WEBAUTHN_USER_VERIFICATION_REQUIREMENT_REQUIRED<br/>WEBAUTHN_USER_VERIFICATION_REQUIREMENT_PREFERRED<br/>WEBAUTHN_USER_VERIFICATION_REQUIREMENT_DISCOURAGED | 0<br/>1<br/>2<br/>3 | Options for the user verification requirement. |
| WEBAUTHN_ATTESTATION_CONVEYANCE_PREFERENCE_ANY<br/>WEBAUTHN_ATTESTATION_CONVEYANCE_PREFERENCE_NONE<br/>WEBAUTHN_ATTESTATION_CONVEYANCE_PREFERENCE_DIRECT<br/>WEBAUTHN_ATTESTATION_CONVEYANCE_PREFERENCE_INDIRECT | 0<br/>1<br/>2<br/>3 | Attestation conveyance preference options. |
| WEBAUTHN_ENTERPRISE_ATTESTATION_NONE<br/>WEBAUTHN_ENTERPRISE_ATTESTATION_VENDOR_FACILITATED<br/>WEBAUTHN_ENTERPRISE_ATTESTATION_PLATFORM_MANAGED | 0<br/>1<br/>2 | Enterprise attestation options. |
| WEBAUTHN_LARGE_BLOB_SUPPORT_NONE<br/>WEBAUTHN_LARGE_BLOB_SUPPORT_REQUIRED<br/>WEBAUTHN_LARGE_BLOB_SUPPORT_PREFERRED | 0<br/>1<br/>2 | Large blob support options. |
| WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS_VERSION_1<br/>WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS_VERSION_2<br/>WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS_VERSION_3<br/>WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS_VERSION_4<br/>WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS_VERSION_5 | 1<br/>2<br/>3<br/>4<br/>5 | The version of the [WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS](ns-webauthn-webauthn_authenticator_make_credential_options.md) structure, to allow for modifications in the future. |
| WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS_CURRENT_VERSION | WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS_VERSION_5 | The current version of the [WEBAUTHN_AUTHENTICATOR_MAKE_CREDENTIAL_OPTIONS](ns-webauthn-webauthn_authenticator_make_credential_options.md) structure. |
| WEBAUTHN_CRED_LARGE_BLOB_OPERATION_NONE<br/>WEBAUTHN_CRED_LARGE_BLOB_OPERATION_GET<br/>WEBAUTHN_CRED_LARGE_BLOB_OPERATION_SET<br/>WEBAUTHN_CRED_LARGE_BLOB_OPERATION_DELETE | 0<br/>1<br/>2<br/>3 | The operation to perform on the large blob. |
| WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_VERSION_1<br/>WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_VERSION_2<br/>WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_VERSION_3<br/>WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_VERSION_4<br/>WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_VERSION_5<br/>WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_VERSION_6 | 1<br/>2<br/>3<br/>4<br/>5<br/>6 | The version of the [WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS](ns-webauthn-webauthn_authenticator_get_assertion_options.md) structure, to allow for modifications in the future. |
| WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_CURRENT_VERSION | WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS_VERSION_6 | The current version of the [WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS](ns-webauthn-webauthn_authenticator_get_assertion_options.md) structure. |
| WEBAUTHN_AUTHENTICATOR_HMAC_SECRET_VALUES_FLAG | 0x00100000 | Flag for the `dwFlags` field in the [WEBAUTHN_AUTHENTICATOR_GET_ASSERTION_OPTIONS](ns-webauthn-webauthn_authenticator_get_assertion_options.md) structure. |
| WEBAUTHN_ATTESTATION_DECODE_NONE<br/>WEBAUTHN_ATTESTATION_DECODE_COMMON | 0<br/>1 | WEBAUTHN_ATTESTATION_DECODE_COMMON supports format types:<ul><li>"packed"</li><li>"fido-u2f"</li></ul> |
| WEBAUTHN_ATTESTATION_VER_TPM_2_0 | "2.0" | The TPM version to use with the attestation. |
| WEBAUTHN_COMMON_ATTESTATION_CURRENT_VERSION | 1 | The version of the [WEBAUTHN_COMMON_ATTESTATION](ns-webauthn-webauthn_common_attestation.md) structure, to allow for modifications in the future. **Note, new fields will be added to the following data structure to support additional attestation format types, such as, TPM. When fields are added, the version will be incremented.** |
| WEBAUTHN_ATTESTATION_TYPE_PACKED<br/>WEBAUTHN_ATTESTATION_TYPE_U2F<br/>WEBAUTHN_ATTESTATION_TYPE_TPM<br/>WEBAUTHN_ATTESTATION_TYPE_NONE | "packed"<br/>"fido-u2f"<br/>"tpm"<br/>"none" | The attestation format type. |
| WEBAUTHN_CREDENTIAL_ATTESTATION_VERSION_1<br/>WEBAUTHN_CREDENTIAL_ATTESTATION_VERSION_2<br/>WEBAUTHN_CREDENTIAL_ATTESTATION_VERSION_3<br/>WEBAUTHN_CREDENTIAL_ATTESTATION_VERSION_4 | 1<br/>2<br/>3<br/>4 | The version of the [WEBAUTHN_CREDENTIAL_ATTESTATION](ns-webauthn-webauthn_credential_attestation.md) structure, to allow for modifications in the future. |
| WEBAUTHN_CREDENTIAL_ATTESTATION_CURRENT_VERSION | WEBAUTHN_CREDENTIAL_ATTESTATION_VERSION_4 | The current version of the [WEBAUTHN_CREDENTIAL_ATTESTATION](ns-webauthn-webauthn_credential_attestation.md) structure. |
| WEBAUTHN_CRED_LARGE_BLOB_STATUS_NONE<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_SUCCESS<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_NOT_SUPPORTED<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_INVALID_DATA<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_INVALID_PARAMETER<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_NOT_FOUND<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_MULTIPLE_CREDENTIALS<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_LACK_OF_SPACE<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_PLATFORM_ERROR<br/>WEBAUTHN_CRED_LARGE_BLOB_STATUS_AUTHENTICATOR_ERROR | 0<br/>1<br/>2<br/>3<br/>4<br/>5<br/>6<br/>7<br/>8<br/>9 | The status of the large blob operation. |
| WEBAUTHN_ASSERTION_VERSION_1<br/>WEBAUTHN_ASSERTION_VERSION_2<br/>WEBAUTHN_ASSERTION_VERSION_3 | 1<br/>2<br/>3 | The version of the [WEBAUTHN_ASSERTION](ns-webauthn-webauthn_assertion.md) structure, to allow for modifications in the future. |
| WEBAUTHN_ASSERTION_CURRENT_VERSION | WEBAUTHN_ASSERTION_VERSION_3 | The current version of the [WEBAUTHN_ASSERTION](ns-webauthn-webauthn_assertion.md) structure. |

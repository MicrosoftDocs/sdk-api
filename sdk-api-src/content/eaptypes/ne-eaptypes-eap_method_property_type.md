---
UID: NE:eaptypes._EAP_METHOD_PROPERTY_TYPE
title: EAP_METHOD_PROPERTY_TYPE (eaptypes.h)
description: Specifies the set of possible EAP method properties.
helpviewer_keywords: ["EAP_METHOD_PROPERTY_TYPE","EAP_METHOD_PROPERTY_TYPE enumeration [EAPHost]","eaphost.eap_method_property_type","eaptypes/EAP_METHOD_PROPERTY_TYPE","eaptypes/emptLegacyMethodPropertyFlag","eaptypes/emptPropCertifiedMethod","eaptypes/emptPropChannelBinding","eaptypes/emptPropCipherSuiteNegotiation","eaptypes/emptPropConfidentiality","eaptypes/emptPropCryptoBinding","eaptypes/emptPropDictionaryAttackResistance","eaptypes/emptPropFastReconnect","eaptypes/emptPropFragmentation","eaptypes/emptPropHiddenMethod","eaptypes/emptPropIdentityPrivacy","eaptypes/emptPropIntegrity","eaptypes/emptPropKeyDerivation","eaptypes/emptPropKeyStrength1024","eaptypes/emptPropKeyStrength128","eaptypes/emptPropKeyStrength256","eaptypes/emptPropKeyStrength512","eaptypes/emptPropKeyStrength64","eaptypes/emptPropMachineAuth","eaptypes/emptPropMethodChaining","eaptypes/emptPropMppeEncryption","eaptypes/emptPropMutualAuth","eaptypes/emptPropNap","eaptypes/emptPropReplayProtection","eaptypes/emptPropSessionIndependence","eaptypes/emptPropSharedStateEquivalence","eaptypes/emptPropStandalone","eaptypes/emptPropSupportsConfig","eaptypes/emptPropTunnelMethod","eaptypes/emptPropUserAuth","eaptypes/emptPropVendorSpecific","emptLegacyMethodPropertyFlag","emptPropCertifiedMethod","emptPropChannelBinding","emptPropCipherSuiteNegotiation","emptPropConfidentiality","emptPropCryptoBinding","emptPropDictionaryAttackResistance","emptPropFastReconnect","emptPropFragmentation","emptPropHiddenMethod","emptPropIdentityPrivacy","emptPropIntegrity","emptPropKeyDerivation","emptPropKeyStrength1024","emptPropKeyStrength128","emptPropKeyStrength256","emptPropKeyStrength512","emptPropKeyStrength64","emptPropMachineAuth","emptPropMethodChaining","emptPropMppeEncryption","emptPropMutualAuth","emptPropNap","emptPropReplayProtection","emptPropSessionIndependence","emptPropSharedStateEquivalence","emptPropStandalone","emptPropSupportsConfig","emptPropTunnelMethod","emptPropUserAuth","emptPropVendorSpecific"]
old-location: eaphost\eap_method_property_type.htm
tech.root: eaphost
ms.assetid: 49a62be4-5a8c-4e44-bdd1-aba37e3e7029
ms.date: 12/05/2018
ms.keywords: EAP_METHOD_PROPERTY_TYPE, EAP_METHOD_PROPERTY_TYPE enumeration [EAPHost], eaphost.eap_method_property_type, eaptypes/EAP_METHOD_PROPERTY_TYPE, eaptypes/emptLegacyMethodPropertyFlag, eaptypes/emptPropCertifiedMethod, eaptypes/emptPropChannelBinding, eaptypes/emptPropCipherSuiteNegotiation, eaptypes/emptPropConfidentiality, eaptypes/emptPropCryptoBinding, eaptypes/emptPropDictionaryAttackResistance, eaptypes/emptPropFastReconnect, eaptypes/emptPropFragmentation, eaptypes/emptPropHiddenMethod, eaptypes/emptPropIdentityPrivacy, eaptypes/emptPropIntegrity, eaptypes/emptPropKeyDerivation, eaptypes/emptPropKeyStrength1024, eaptypes/emptPropKeyStrength128, eaptypes/emptPropKeyStrength256, eaptypes/emptPropKeyStrength512, eaptypes/emptPropKeyStrength64, eaptypes/emptPropMachineAuth, eaptypes/emptPropMethodChaining, eaptypes/emptPropMppeEncryption, eaptypes/emptPropMutualAuth, eaptypes/emptPropNap, eaptypes/emptPropReplayProtection, eaptypes/emptPropSessionIndependence, eaptypes/emptPropSharedStateEquivalence, eaptypes/emptPropStandalone, eaptypes/emptPropSupportsConfig, eaptypes/emptPropTunnelMethod, eaptypes/emptPropUserAuth, eaptypes/emptPropVendorSpecific, emptLegacyMethodPropertyFlag, emptPropCertifiedMethod, emptPropChannelBinding, emptPropCipherSuiteNegotiation, emptPropConfidentiality, emptPropCryptoBinding, emptPropDictionaryAttackResistance, emptPropFastReconnect, emptPropFragmentation, emptPropHiddenMethod, emptPropIdentityPrivacy, emptPropIntegrity, emptPropKeyDerivation, emptPropKeyStrength1024, emptPropKeyStrength128, emptPropKeyStrength256, emptPropKeyStrength512, emptPropKeyStrength64, emptPropMachineAuth, emptPropMethodChaining, emptPropMppeEncryption, emptPropMutualAuth, emptPropNap, emptPropReplayProtection, emptPropSessionIndependence, emptPropSharedStateEquivalence, emptPropStandalone, emptPropSupportsConfig, emptPropTunnelMethod, emptPropUserAuth, emptPropVendorSpecific
req.header: eaptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: EAP_METHOD_PROPERTY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_METHOD_PROPERTY_TYPE
 - eaptypes/_EAP_METHOD_PROPERTY_TYPE
 - EAP_METHOD_PROPERTY_TYPE
 - eaptypes/EAP_METHOD_PROPERTY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EapTypes.h
api_name:
 - EAP_METHOD_PROPERTY_TYPE
---

# EAP_METHOD_PROPERTY_TYPE enumeration


## -description

The <b>EAP_METHOD_PROPERTY_TYPE</b> enumeration specifies the set of possible EAP method properties.

## -enum-fields

### -field emptPropCipherSuiteNegotiation:0

Boolean method property for specifying the support for cipher suite negotiation.

### -field emptPropMutualAuth

Boolean method property for specifying the support for mutual authentication.

### -field emptPropIntegrity

Boolean method property for specifying the support for message integrity.

### -field emptPropReplayProtection

Boolean method property for specifying the support for replay protection.

### -field emptPropConfidentiality

Boolean method property for specifying the support for encrypting EAP messages.

### -field emptPropKeyDerivation

Boolean method property for specifying the support for deriving exportable keying materials.

### -field emptPropKeyStrength64

Boolean method property for specifying the support for key length of at least 64 bits.

### -field emptPropKeyStrength128

Boolean method property for specifying the support for key length of at least 128 bits.

### -field emptPropKeyStrength256

Boolean method property for specifying the support for key length of at least 256 bits.

### -field emptPropKeyStrength512

Boolean method property for specifying the support for key length of at least 512 bits.

### -field emptPropKeyStrength1024

Boolean method property for specifying the support for key length of at least 1024 bits.

### -field emptPropDictionaryAttackResistance

Boolean method property for specifying the support for preventing offline attack that has a work factor based on the number of passwords in an attacker’s dictionary.

### -field emptPropFastReconnect

Boolean method property for specifying the support for establishing a security association in a smaller number of round trips by using the cached parameters of a previous successful authentication.

### -field emptPropCryptoBinding

Boolean method property for specifying the support for preventing man-in-the-middle attacks in a tunneling method. The method supporting cryptobinding demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.

### -field emptPropSessionIndependence

Boolean method property for specifying that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.

### -field emptPropFragmentation

Boolean method property for specifying the support for fragmentation and reassembly of EAP packets exceeding the MTU size.

### -field emptPropChannelBinding

Boolean method property for specifying the ability to communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms, such as an Authentication, Authorization, and Accounting (AAA) protocol or the lower layer protocol.

### -field emptPropNap

Boolean method property for specifying the support for Network Access Protection.

### -field emptPropStandalone

Boolean method property for specifying the support for execution of the method on a standalone computer.

### -field emptPropMppeEncryption

Boolean method property for specifying the support for Microsoft Point-to-Point Encryption (MPPE) protocol encryption.

### -field emptPropTunnelMethod

Boolean method property for specifying the ability of the method to tunnel other EAP methods.

### -field emptPropSupportsConfig

Boolean method property for specifying the support for method configuration and user interface.

### -field emptPropCertifiedMethod

Boolean method property for specifying if the method was certified by the EAP Certification Program (ECP).

### -field emptPropHiddenMethod

Boolean method property for specifying a hidden method.

### -field emptPropMachineAuth

Boolean method property for specifying the support for computer authentication.

### -field emptPropUserAuth

Boolean method property for specifying the support for user authentication.

### -field emptPropIdentityPrivacy

Boolean method property for specifying the support for identity privacy.

### -field emptPropMethodChaining

Boolean method property for specifying the support for method chaining.

### -field emptPropSharedStateEquivalence

Boolean method property for specifying the support for shared state equivalence as defined in RFC4017.

### -field emptLegacyMethodPropertyFlag:31

<b>DWORD</b> property method for values sent prior to Windows 7.

### -field emptPropVendorSpecific

String property method for specifying any vendor-specific property of the EAP method.

### -field v1_enum

## -see-also

[EAPHost Supplicant Enumerations](/windows/win32/eaphost/eap-host-supplicant-enumerations)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_property">EAP_METHOD_PROPERTY</a>



<a href="/windows/desktop/api/eaptypes/ne-eaptypes-eap_method_property_value_type">EAP_METHOD_PROPERTY_VALUE_TYPE</a>

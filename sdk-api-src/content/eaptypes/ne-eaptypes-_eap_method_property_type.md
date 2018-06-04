---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _EAP_METHOD_PROPERTY_TYPE enumeration


## -description


The <b>EAP_METHOD_PROPERTY_TYPE</b> enumeration specifies the set of possible EAP method properties.


## -enum-fields




### -field emptPropCipherSuiteNegotiation

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


### -field emptLegacyMethodPropertyFlag

<b>DWORD</b> property method for values sent prior to Windows 7.


### -field emptPropVendorSpecific

String property method for specifying any vendor-specific property of the EAP method.


### -field v1_enum




## -see-also




<a href="https://msdn.microsoft.com/ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014">EAPHost Supplicant Enumerations</a>



<a href="https://msdn.microsoft.com/df8c9ba2-e1c5-4011-bdbe-1d04765d19cd">EAP_METHOD_PROPERTY</a>



<a href="https://msdn.microsoft.com/17ef654a-d4a0-45ba-a49d-45add8e78b28">EAP_METHOD_PROPERTY_VALUE_TYPE</a>
 

 


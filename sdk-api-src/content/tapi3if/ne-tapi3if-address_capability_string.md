---
UID: NE:tapi3if.ADDRESS_CAPABILITY_STRING
title: ADDRESS_CAPABILITY_STRING (tapi3if.h)
description: The ADDRESS_CAPABILITY_STRING enum is used to check on address capabilities which are described by strings.
helpviewer_keywords: ["ACS_ADDRESSDEVICESPECIFIC","ACS_LINEDEVICESPECIFIC","ACS_PERMANENTDEVICEGUID","ACS_PROTOCOL","ACS_PROVIDERSPECIFIC","ACS_SWITCHSPECIFIC","ADDRESS_CAPABILITY_STRING","ADDRESS_CAPABILITY_STRING enumeration [TAPI 2.2]","_tapi3_address_capability_string","tapi3.address_capability_string","tapi3if/ACS_ADDRESSDEVICESPECIFIC","tapi3if/ACS_LINEDEVICESPECIFIC","tapi3if/ACS_PERMANENTDEVICEGUID","tapi3if/ACS_PROTOCOL","tapi3if/ACS_PROVIDERSPECIFIC","tapi3if/ACS_SWITCHSPECIFIC","tapi3if/ADDRESS_CAPABILITY_STRING"]
old-location: tapi3\address_capability_string.htm
tech.root: tapi3
ms.assetid: c0afe710-ae6d-4f32-a691-956f8d6fea05
ms.date: 12/05/2018
ms.keywords: ACS_ADDRESSDEVICESPECIFIC, ACS_LINEDEVICESPECIFIC, ACS_PERMANENTDEVICEGUID, ACS_PROTOCOL, ACS_PROVIDERSPECIFIC, ACS_SWITCHSPECIFIC, ADDRESS_CAPABILITY_STRING, ADDRESS_CAPABILITY_STRING enumeration [TAPI 2.2], _tapi3_address_capability_string, tapi3.address_capability_string, tapi3if/ACS_ADDRESSDEVICESPECIFIC, tapi3if/ACS_LINEDEVICESPECIFIC, tapi3if/ACS_PERMANENTDEVICEGUID, tapi3if/ACS_PROTOCOL, tapi3if/ACS_PROVIDERSPECIFIC, tapi3if/ACS_SWITCHSPECIFIC, tapi3if/ADDRESS_CAPABILITY_STRING
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADDRESS_CAPABILITY_STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADDRESS_CAPABILITY_STRING
 - tapi3if/ADDRESS_CAPABILITY_STRING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - ADDRESS_CAPABILITY_STRING
---

# ADDRESS_CAPABILITY_STRING enumeration


## -description

The 
<b>ADDRESS_CAPABILITY_STRING</b> enum is used to check on address capabilities which are described by strings.

## -enum-fields

### -field ACS_PROTOCOL:0

Describes a protocol-specific capability. The value is returned as a GUID in string format. For possible values, see 
<a href="/windows/desktop/Tapi/tapiprotocol--constants">TAPIPROTOCOL_</a>. A TSP may define additional values. Corresponds to the <b>ProtocolGuid</b> member of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

### -field ACS_ADDRESSDEVICESPECIFIC

Describes an address device-specific capability. The value is TSP dependent and can be a structure, a string, or some other type. An application should use the <b>BSTR</b> pointer received from Tapi3.dll as a pointer to an array of bytes (a buffer), and then interpret the buffer according to TSP specifications. Corresponds to the <b>dwDevSpecific</b> and <b>dwDevSpecificSize</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a> structure.

### -field ACS_LINEDEVICESPECIFIC

Describes a line device-specific capability. The value is TSP dependent and can be a structure, a string, or some other type. An application should use the <b>BSTR</b> pointer received from Tapi3.dll as a pointer to an array of bytes (a buffer), and then interpret the buffer according to TSP specifications. Corresponds to the <b>dwDevSpecific</b> and <b>dwDevSpecificSize</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

### -field ACS_PROVIDERSPECIFIC

Describes a provider-specific capability. The value is a plain string. It can be used with regular <b>BSTR</b> functions for operations such as printing and concatenating. A specific TSP might included embedded <b>NULL</b> characters inside these strings. If so, an application should take care when printing the value. If the embedded <b>NULL</b> characters are not replaced with blanks, the strings will appear truncated when printed. Corresponds to the <b>dwProviderInfoSize</b> and <b>dwProviderInfoOffset</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

### -field ACS_SWITCHSPECIFIC

Describes a switch-specific capability. The value is a plain string. It can be used with regular <b>BSTR</b> functions for operations such as printing and concatenating. A specific TSP might included embedded <b>NULL</b> characters inside these strings. If so, an application should take care when printing the value. If the embedded <b>NULL</b> characters are not replaced with blanks, the strings will appear truncated when printed. Corresponds to the <b>dwSwitchInfoSize</b> and <b>dwSwitchInfoOffset</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

### -field ACS_PERMANENTDEVICEGUID

Describes the GUID of a permanent device. The value is returned as a GUID in string format. This identifier must remain stable throughout, including operating system upgrades. Corresponds to the <b>PermanentLineGuid</b> member of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapabilitystring">ITAddressCapabilities::get_AddressCapabilityString</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineaddresscaps">LINEADDRESSCAPS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/tapiprotocol--constants">TAPIPROTOCOL_</a>

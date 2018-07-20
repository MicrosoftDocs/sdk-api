---
UID: NE:tapi3if.ADDRESS_CAPABILITY_STRING
title: ADDRESS_CAPABILITY_STRING
author: windows-sdk-content
description: The ADDRESS_CAPABILITY_STRING enum is used to check on address capabilities which are described by strings.
old-location: tapi3\address_capability_string.htm
old-project: tapi
ms.assetid: c0afe710-ae6d-4f32-a691-956f8d6fea05
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ACS_ADDRESSDEVICESPECIFIC, ACS_LINEDEVICESPECIFIC, ACS_PERMANENTDEVICEGUID, ACS_PROTOCOL, ACS_PROVIDERSPECIFIC, ACS_SWITCHSPECIFIC, ADDRESS_CAPABILITY_STRING, ADDRESS_CAPABILITY_STRING enumeration [TAPI 2.2], _tapi3_address_capability_string, tapi3.address_capability_string, tapi3if/ACS_ADDRESSDEVICESPECIFIC, tapi3if/ACS_LINEDEVICESPECIFIC, tapi3if/ACS_PERMANENTDEVICEGUID, tapi3if/ACS_PROTOCOL, tapi3if/ACS_PROVIDERSPECIFIC, tapi3if/ACS_SWITCHSPECIFIC, tapi3if/ADDRESS_CAPABILITY_STRING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: ADDRESS_CAPABILITY_STRING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - ADDRESS_CAPABILITY_STRING
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ADDRESS_CAPABILITY_STRING enumeration


## -description


The 
<b>ADDRESS_CAPABILITY_STRING</b> enum is used to check on address capabilities which are described by strings.


## -enum-fields




### -field ACS_PROTOCOL

Describes a protocol-specific capability. The value is returned as a GUID in string format. For possible values, see 
<a href="https://msdn.microsoft.com/4704eedb-12e7-440e-b1ca-2afd78d2499d">TAPIPROTOCOL_</a>. A TSP may define additional values. Corresponds to the <b>ProtocolGuid</b> member of TAPI 2's 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure.


### -field ACS_ADDRESSDEVICESPECIFIC

Describes an address device-specific capability. The value is TSP dependent and can be a structure, a string, or some other type. An application should use the <b>BSTR</b> pointer received from Tapi3.dll as a pointer to an array of bytes (a buffer), and then interpret the buffer according to TSP specifications. Corresponds to the <b>dwDevSpecific</b> and <b>dwDevSpecificSize</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a> structure.


### -field ACS_LINEDEVICESPECIFIC

Describes a line device-specific capability. The value is TSP dependent and can be a structure, a string, or some other type. An application should use the <b>BSTR</b> pointer received from Tapi3.dll as a pointer to an array of bytes (a buffer), and then interpret the buffer according to TSP specifications. Corresponds to the <b>dwDevSpecific</b> and <b>dwDevSpecificSize</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure.


### -field ACS_PROVIDERSPECIFIC

Describes a provider-specific capability. The value is a plain string. It can be used with regular <b>BSTR</b> functions for operations such as printing and concatenating. A specific TSP might included embedded <b>NULL</b> characters inside these strings. If so, an application should take care when printing the value. If the embedded <b>NULL</b> characters are not replaced with blanks, the strings will appear truncated when printed. Corresponds to the <b>dwProviderInfoSize</b> and <b>dwProviderInfoOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure.


### -field ACS_SWITCHSPECIFIC

Describes a switch-specific capability. The value is a plain string. It can be used with regular <b>BSTR</b> functions for operations such as printing and concatenating. A specific TSP might included embedded <b>NULL</b> characters inside these strings. If so, an application should take care when printing the value. If the embedded <b>NULL</b> characters are not replaced with blanks, the strings will appear truncated when printed. Corresponds to the <b>dwSwitchInfoSize</b> and <b>dwSwitchInfoOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure.


### -field ACS_PERMANENTDEVICEGUID

Describes the GUID of a permanent device. The value is returned as a GUID in string format. This identifier must remain stable throughout, including operating system upgrades. Corresponds to the <b>PermanentLineGuid</b> member of TAPI 2's 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/9ec4c25e-700b-4aed-97ff-e7cb420fdf96">ITAddressCapabilities::get_AddressCapabilityString</a>



<a href="https://msdn.microsoft.com/c1fe1aaf-2f50-4423-bacf-6a3cf218a809">LINEADDRESSCAPS</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/4704eedb-12e7-440e-b1ca-2afd78d2499d">TAPIPROTOCOL_</a>
 

 


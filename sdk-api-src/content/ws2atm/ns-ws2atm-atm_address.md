---
UID: NS:ws2atm.ATM_ADDRESS
title: ATM_ADDRESS (ws2atm.h)
description: The ATM_ADDRESS structure holds ATM address data for ATM-based sockets.
helpviewer_keywords: ["ATM_ADDRESS","ATM_ADDRESS structure [Winsock]","ATM_CALLED_PARTY_NUMBER_IE","ATM_CALLED_PARTY_SUBADDRESS_IE","ATM_CALLING_PARTY_SUBADDRESS_IE","_win32_atm_address_2","winsock.atm_address_2","ws2atm/ATM_ADDRESS"]
old-location: winsock\atm_address_2.htm
tech.root: WinSock
ms.assetid: 794d4070-45d7-41c3-8229-660ba3c5f72a
ms.date: 12/05/2018
ms.keywords: ATM_ADDRESS, ATM_ADDRESS structure [Winsock], ATM_CALLED_PARTY_NUMBER_IE, ATM_CALLED_PARTY_SUBADDRESS_IE, ATM_CALLING_PARTY_SUBADDRESS_IE, _win32_atm_address_2, winsock.atm_address_2, ws2atm/ATM_ADDRESS
req.header: ws2atm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ATM_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ATM_ADDRESS
 - ws2atm/ATM_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2atm.h
api_name:
 - ATM_ADDRESS
---

# ATM_ADDRESS structure


## -description

The 
<b>ATM_ADDRESS</b> structure holds ATM address data for ATM-based sockets.

## -struct-fields

### -field AddressType

Type of end-system ATM address.

### -field NumofDigits

Number of digits in the <b>Addr</b> parameter.

### -field Addr

Array representing the ATM address.

## -remarks

For ATM_E164, enter the numbered digits in the same order in which they would be entered on a numeric keypad; that is, the number digit that would be entered first is located in <b>addr</b>. Digits are coded in IA5 characters. Bit 8 is set to zero.

For ATM_NSAP, code the address using Binary Coded Decimal (BCD) as defined in the ATM Forum UNI 3.1. The <b>NumofDigits</b> field is ignored in this case, and the NSAP-style address always contains 20 bytes.

A value of SAP_FIELD_ANY in <b>AddressType</b> indicates that the <b>satm_number</b> field is a wildcard. There are two more specialized wildcard values: SAP_FIELD_ANY_AESA_SEL and SAP_FIELD_ANY_AESA_REST. SAP_FIELD_ANY_AESA_SEL means that this is an NSAP-style ATM Endsystem Address and the selector octet is set as a wildcard. SAP_FIELD_ANY_AESA_REST means that this is an NSAP-style ATM Endsystem Address and all the octets except for the selector octet are set as wildcards.

## -see-also

<a href="/windows/desktop/api/ws2atm/ns-ws2atm-sockaddr_atm">sockaddr_atm</a>


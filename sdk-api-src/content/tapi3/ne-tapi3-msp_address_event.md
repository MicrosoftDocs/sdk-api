---
UID: NE:tapi3.__MIDL___MIDL_itf_tapi3_0000_0018_0001
title: MSP_ADDRESS_EVENT (tapi3.h)
description: The MSP_ADDRESS_EVENT constant is returned within the MSP_EVENT_INFO struct by the GetEvent method when MSP_EVENT is ME_ADDRESS_EVENT.
helpviewer_keywords: ["ADDRESS_TERMINAL_AVAILABLE","ADDRESS_TERMINAL_UNAVAILABLE","MSP_ADDRESS_EVENT","MSP_ADDRESS_EVENT enumeration [TAPI 2.2]","_tapi3_msp_address_event","msp/ADDRESS_TERMINAL_AVAILABLE","msp/ADDRESS_TERMINAL_UNAVAILABLE","msp/MSP_ADDRESS_EVENT","tapi3.msp_address_event"]
old-location: tapi3\msp_address_event.htm
tech.root: tapi3
ms.assetid: 35aecd05-badd-4509-92e5-1936ca075c37
ms.date: 12/05/2018
ms.keywords: ADDRESS_TERMINAL_AVAILABLE, ADDRESS_TERMINAL_UNAVAILABLE, MSP_ADDRESS_EVENT, MSP_ADDRESS_EVENT enumeration [TAPI 2.2], _tapi3_msp_address_event, msp/ADDRESS_TERMINAL_AVAILABLE, msp/ADDRESS_TERMINAL_UNAVAILABLE, msp/MSP_ADDRESS_EVENT, tapi3.msp_address_event
req.header: tapi3.h
req.include-header: Tapi3.h
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
req.typenames: MSP_ADDRESS_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_tapi3_0000_0018_0001
 - tapi3/__MIDL___MIDL_itf_tapi3_0000_0018_0001
 - MSP_ADDRESS_EVENT
 - tapi3/MSP_ADDRESS_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msp.h
api_name:
 - MSP_ADDRESS_EVENT
---

# MSP_ADDRESS_EVENT enumeration


## -description

The <b>MSP_ADDRESS_EVENT</b> constant is returned within the 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a> struct by the 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">GetEvent</a> method when 
<a href="/windows/win32/api/msp/ne-msp-msp_event">MSP_EVENT</a> is ME_ADDRESS_EVENT.

## -enum-fields

### -field ADDRESS_TERMINAL_AVAILABLE:0

A new terminal arrived by PNP.

### -field ADDRESS_TERMINAL_UNAVAILABLE

A terminal has been removed by PNP.

## -see-also

<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">ITMSPAddress::GetEvent</a>



<a href="/windows/win32/api/msp/ne-msp-msp_event">MSP_EVENT</a>



<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>

---
UID: NE:msp.__MIDL___MIDL_itf_msp_0000_0000_0004
title: MSP_EVENT (msp.h)
description: The MSP_EVENT enumerator defines the type of event information contained in MSP_EVENT_INFO.
helpviewer_keywords: ["ME_ADDRESS_EVENT","ME_CALL_EVENT","ME_PRIVATE_EVENT","ME_TSP_DATA","MSP_EVENT","MSP_EVENT enumeration [TAPI 2.2]","_tapi3_msp_event","msp/ME_ADDRESS_EVENT","msp/ME_CALL_EVENT","msp/ME_PRIVATE_EVENT","msp/ME_TSP_DATA","msp/MSP_EVENT","tapi3.msp_event"]
old-location: tapi3\msp_event.htm
tech.root: tapi3
ms.assetid: 53e19eff-b5f0-43fd-b59b-e85e75220282
ms.date: 12/05/2018
ms.keywords: ME_ADDRESS_EVENT, ME_CALL_EVENT, ME_PRIVATE_EVENT, ME_TSP_DATA, MSP_EVENT, MSP_EVENT enumeration [TAPI 2.2], _tapi3_msp_event, msp/ME_ADDRESS_EVENT, msp/ME_CALL_EVENT, msp/ME_PRIVATE_EVENT, msp/ME_TSP_DATA, msp/MSP_EVENT, tapi3.msp_event
req.header: msp.h
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
req.typenames: MSP_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msp_0000_0000_0004
 - msp/__MIDL___MIDL_itf_msp_0000_0000_0004
 - MSP_EVENT
 - msp/MSP_EVENT
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
 - MSP_EVENT
---

# MSP_EVENT enumeration


## -description

The <b>MSP_EVENT</b> enumerator defines the type of event information contained in 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>.

## -enum-fields

### -field ME_ADDRESS_EVENT:0

The event buffer is an 
<a href="/previous-versions/windows/desktop/legacy/ms733454(v=vs.85)">MSP_ADDRESS_EVENT_INFO</a> structure.

### -field ME_CALL_EVENT

The event buffer is an 
<a href="/previous-versions/windows/desktop/legacy/ms733464(v=vs.85)">MSP_CALL_EVENT_INFO</a> structure.

### -field ME_TSP_DATA

The event buffer is an 
<a href="/previous-versions/windows/desktop/legacy/ms733475(v=vs.85)">MSP_TSP_DATA</a> structure.

### -field ME_PRIVATE_EVENT

The event buffer is an 
<a href="/previous-versions/windows/desktop/legacy/ms733472(v=vs.85)">MSP_PRIVATE_EVENT_INFO</a> structure.

### -field ME_ASR_TERMINAL_EVENT

### -field ME_TTS_TERMINAL_EVENT

### -field ME_FILE_TERMINAL_EVENT

### -field ME_TONE_TERMINAL_EVENT

## -see-also

<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">ITMSPAddress::GetEvent</a>



<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>

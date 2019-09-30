---
UID: NE:tapi3.__MIDL___MIDL_itf_tapi3_0000_0018_0004
title: MSP_EVENT (tapi3.h)
author: windows-sdk-content
description: The MSP_EVENT enumerator defines the type of event information contained in MSP_EVENT_INFO.
old-location: tapi3\msp_event.htm
tech.root: Tapi
ms.assetid: 53e19eff-b5f0-43fd-b59b-e85e75220282
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ME_ADDRESS_EVENT, ME_CALL_EVENT, ME_PRIVATE_EVENT, ME_TSP_DATA, MSP_EVENT, MSP_EVENT enumeration [TAPI 2.2], _tapi3_msp_event, msp/ME_ADDRESS_EVENT, msp/ME_CALL_EVENT, msp/ME_PRIVATE_EVENT, msp/ME_TSP_DATA, msp/MSP_EVENT, tapi3.msp_event
ms.topic: enum
f1_keywords: 
 - "tapi3/MSP_EVENT"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msp.h
api_name:
 - MSP_EVENT
targetos: Windows
req.typenames: MSP_EVENT
req.redist: 
ms.custom: 19H1
---

# MSP_EVENT enumeration


## -description


The <b>MSP_EVENT</b> enumerator defines the type of event information contained in 
<a href="https://docs.microsoft.com/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>.


## -enum-fields




### -field ME_ADDRESS_EVENT

The event buffer is an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms733454(v=vs.85)">MSP_ADDRESS_EVENT_INFO</a> structure.


### -field ME_CALL_EVENT

The event buffer is an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms733464(v=vs.85)">MSP_CALL_EVENT_INFO</a> structure.


### -field ME_TSP_DATA

The event buffer is an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms733475(v=vs.85)">MSP_TSP_DATA</a> structure.


### -field ME_PRIVATE_EVENT

The event buffer is an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms733472(v=vs.85)">MSP_PRIVATE_EVENT_INFO</a> structure.


### -field ME_ASR_TERMINAL_EVENT


### -field ME_TTS_TERMINAL_EVENT


### -field ME_FILE_TERMINAL_EVENT


### -field ME_TONE_TERMINAL_EVENT




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">ITMSPAddress::GetEvent</a>



<a href="https://docs.microsoft.com/windows/win32/api/msp/ns-msp-msp_event_info">MSP_EVENT_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 


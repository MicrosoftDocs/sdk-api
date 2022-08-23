---
UID: NS:msp.__MIDL___MIDL_itf_msp_0000_0000_0005
title: MSP_EVENT_INFO (msp.h)
description: The MSP_EVENT_INFO (msp.h) structure defines the type of event returned by the GetEvent method.
helpviewer_keywords: ["MSP_EVENT_INFO","MSP_EVENT_INFO structure [TAPI 2.2]","__MIDL___MIDL_itf_tapi3_0000_0018_0005","_tapi3_msp_event_info","msp/MSP_EVENT_INFO","tapi3.msp_event_info"]
old-location: tapi3\msp_event_info.htm
tech.root: tapi3
ms.assetid: 5286fbe6-3553-42f1-82e6-5bb6f75f3305
ms.date: 08/08/2022
ms.keywords: MSP_EVENT_INFO, MSP_EVENT_INFO structure [TAPI 2.2], __MIDL___MIDL_itf_tapi3_0000_0018_0005, _tapi3_msp_event_info, msp/MSP_EVENT_INFO, tapi3.msp_event_info
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
req.typenames: MSP_EVENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msp_0000_0000_0005
 - msp/__MIDL___MIDL_itf_msp_0000_0000_0005
 - MSP_EVENT_INFO
 - msp/MSP_EVENT_INFO
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
 - MSP_EVENT_INFO
---

# MSP_EVENT_INFO structure


## -description

The 
<b>MSP_EVENT_INFO</b> structure defines the type of event returned by the 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">GetEvent</a> method.

## -struct-fields

### -field dwSize

Total size of structure returned.

### -field Event

### -field hCall

MSP handle; may be <b>NULL</b>.

### -field MSP_ADDRESS_EVENT_INFO

Struct returned if MSP event is ME_ADDRESS_EVENT.

### -field MSP_ADDRESS_EVENT_INFO.Type

Describes the 
<a href="/windows/win32/api/msp/ne-msp-msp_address_event">msp address event</a> of the event that has occurred.

### -field MSP_ADDRESS_EVENT_INFO.pTerminal

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

### -field MSP_CALL_EVENT_INFO

Struct returned if MSP event is ME_CALL_EVENT.

### -field MSP_CALL_EVENT_INFO.Type

Indicates type of 
<a href="/windows/win32/api/msp/ne-msp-msp_call_event">MSP_CALL_EVENT</a> that has occurred.

### -field MSP_CALL_EVENT_INFO.Cause

### -field MSP_CALL_EVENT_INFO.pStream

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface on which event occurred.

### -field MSP_CALL_EVENT_INFO.pTerminal

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface on which event occurred.

### -field MSP_CALL_EVENT_INFO.hrError

Indicates error, if one has happened.

### -field MSP_TSP_DATA

Struct returned if MSP event is ME_TSP_DATA.

### -field MSP_TSP_DATA.dwBufferSize

Size of buffer returned.

Buffer size, in bytes.

### -field MSP_TSP_DATA.pBuffer

Pointer to buffer.

### -field MSP_PRIVATE_EVENT_INFO

Struct returned if MSP event is ME_PRIVATE_EVENT.

### -field MSP_PRIVATE_EVENT_INFO.pEvent

MSP event.



##### pEvent.pEvent

Pointer to <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface of private object on which event has occurred.

### -field MSP_PRIVATE_EVENT_INFO.lEventCode

### -field MSP_FILE_TERMINAL_EVENT_INFO

### -field MSP_FILE_TERMINAL_EVENT_INFO.pParentFileTerminal

### -field MSP_FILE_TERMINAL_EVENT_INFO.pFileTrack

### -field MSP_FILE_TERMINAL_EVENT_INFO.TerminalMediaState

### -field MSP_FILE_TERMINAL_EVENT_INFO.ftecEventCause

### -field MSP_FILE_TERMINAL_EVENT_INFO.hrErrorCode

### -field MSP_ASR_TERMINAL_EVENT_INFO

### -field MSP_ASR_TERMINAL_EVENT_INFO.pASRTerminal

### -field MSP_ASR_TERMINAL_EVENT_INFO.hrErrorCode

### -field MSP_TTS_TERMINAL_EVENT_INFO

### -field MSP_TTS_TERMINAL_EVENT_INFO.pTTSTerminal

### -field MSP_TTS_TERMINAL_EVENT_INFO.hrErrorCode

### -field MSP_TONE_TERMINAL_EVENT_INFO

### -field MSP_TONE_TERMINAL_EVENT_INFO.pToneTerminal

### -field MSP_TONE_TERMINAL_EVENT_INFO.hrErrorCode

## -see-also

<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-getevent">ITMSPAddress::GetEvent</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>

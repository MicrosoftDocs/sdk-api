---
UID: NS:msp.__MIDL___MIDL_itf_msp_0000_0000_0005
title: "__MIDL___MIDL_itf_msp_0000_0000_0005"
author: windows-driver-content
description: The MSP_EVENT_INFO structure defines the type of event returned by the GetEvent method.
old-location: tapi3\msp_event_info.htm
old-project: Tapi
ms.assetid: 5286fbe6-3553-42f1-82e6-5bb6f75f3305
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MSP_EVENT_INFO, MSP_EVENT_INFO structure [TAPI 2.2], __MIDL___MIDL_itf_msp_0000_0000_0005, __MIDL___MIDL_itf_tapi3_0000_0018_0005, _tapi3_msp_event_info, msp/MSP_EVENT_INFO, tapi3.msp_event_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: MSP_EVENT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	msp.h
api_name:
-	MSP_EVENT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_msp_0000_0000_0005 structure


## -description


The 
<b>MSP_EVENT_INFO</b> structure defines the type of event returned by the 
<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">GetEvent</a> method.


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
<a href="https://msdn.microsoft.com/35aecd05-badd-4509-92e5-1936ca075c37">msp address event</a> of the event that has occurred.


### -field MSP_ADDRESS_EVENT_INFO.pTerminal

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


### -field MSP_CALL_EVENT_INFO

Struct returned if MSP event is ME_CALL_EVENT.


### -field MSP_CALL_EVENT_INFO.Type

Indicates type of 
<a href="https://msdn.microsoft.com/c1bbc75e-04ad-4db4-9730-abbbf89306dd">MSP_CALL_EVENT</a> that has occurred.


### -field MSP_CALL_EVENT_INFO.Cause

 


### -field MSP_CALL_EVENT_INFO.pStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface on which event occurred.


### -field MSP_CALL_EVENT_INFO.pTerminal

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface on which event occurred.


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

Pointer to <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface of private object on which event has occurred.


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




<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">ITMSPAddress::GetEvent</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 


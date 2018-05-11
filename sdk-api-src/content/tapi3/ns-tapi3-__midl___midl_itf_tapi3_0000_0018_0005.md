---
UID: NS:tapi3.__MIDL___MIDL_itf_tapi3_0000_0018_0005
title: "__MIDL___MIDL_itf_tapi3_0000_0018_0005"
author: windows-driver-content
description: The MSP_EVENT_INFO structure defines the type of event returned by the GetEvent method.
old-location: tapi3\msp_event_info.htm
old-project: Tapi
ms.assetid: 5286fbe6-3553-42f1-82e6-5bb6f75f3305
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MSP_EVENT_INFO, MSP_EVENT_INFO structure [TAPI 2.2], __MIDL___MIDL_itf_tapi3_0000_0018_0005, _tapi3_msp_event_info, msp/MSP_EVENT_INFO, tapi3.msp_event_info
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_tapi3_0000_0018_0005 structure


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

 


### -field MSP_ADDRESS_EVENT_INFO.pTerminal

 


### -field MSP_CALL_EVENT_INFO

Struct returned if MSP event is ME_CALL_EVENT.


### -field MSP_CALL_EVENT_INFO.Type

 


### -field MSP_CALL_EVENT_INFO.Cause

 


### -field MSP_CALL_EVENT_INFO.pStream

 


### -field MSP_CALL_EVENT_INFO.pTerminal

 


### -field MSP_CALL_EVENT_INFO.hrError

 


### -field MSP_TSP_DATA

Struct returned if MSP event is ME_TSP_DATA.


### -field MSP_TSP_DATA.dwBufferSize

Buffer size, in bytes.


### -field MSP_TSP_DATA.pBuffer

 


### -field MSP_PRIVATE_EVENT_INFO

Struct returned if MSP event is ME_PRIVATE_EVENT.


### -field MSP_PRIVATE_EVENT_INFO.pEvent

MSP event.


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
 

 


---
UID: NE:msp.__MIDL___MIDL_itf_msp_0000_0000_0004
title: "__MIDL___MIDL_itf_msp_0000_0000_0004"
author: windows-sdk-content
description: The MSP_EVENT enumerator defines the type of event information contained in MSP_EVENT_INFO.
old-location: tapi3\msp_event.htm
tech.root: tapi
ms.assetid: 53e19eff-b5f0-43fd-b59b-e85e75220282
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ME_ADDRESS_EVENT, ME_CALL_EVENT, ME_PRIVATE_EVENT, ME_TSP_DATA, MSP_EVENT, MSP_EVENT enumeration [TAPI 2.2], __MIDL___MIDL_itf_msp_0000_0000_0004, _tapi3_msp_event, msp/ME_ADDRESS_EVENT, msp/ME_CALL_EVENT, msp/ME_PRIVATE_EVENT, msp/ME_TSP_DATA, msp/MSP_EVENT, tapi3.msp_event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msp.h
api_name:
 - MSP_EVENT
product: Windows
targetos: Windows
req.typenames: MSP_EVENT
req.redist: 
---

# __MIDL___MIDL_itf_msp_0000_0000_0004 enumeration


## -description


The <b>MSP_EVENT</b> enumerator defines the type of event information contained in 
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a>.


## -enum-fields




### -field ME_ADDRESS_EVENT

The event buffer is an 
<a href="https://msdn.microsoft.com/c4c882cd-8c7e-4860-aa29-32a561f4d135">MSP_ADDRESS_EVENT_INFO</a> structure.


### -field ME_CALL_EVENT

The event buffer is an 
<a href="https://msdn.microsoft.com/9c1d238a-0625-4aaf-a372-18693a2d4b4a">MSP_CALL_EVENT_INFO</a> structure.


### -field ME_TSP_DATA

The event buffer is an 
<a href="https://msdn.microsoft.com/9c405c1d-1729-4c3b-9656-977b9f78b9d7">MSP_TSP_DATA</a> structure.


### -field ME_PRIVATE_EVENT

The event buffer is an 
<a href="https://msdn.microsoft.com/4f572432-398e-48f6-97cc-25f985ca869a">MSP_PRIVATE_EVENT_INFO</a> structure.


### -field ME_ASR_TERMINAL_EVENT


### -field ME_TTS_TERMINAL_EVENT


### -field ME_FILE_TERMINAL_EVENT


### -field ME_TONE_TERMINAL_EVENT




## -see-also




<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">ITMSPAddress::GetEvent</a>



<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 


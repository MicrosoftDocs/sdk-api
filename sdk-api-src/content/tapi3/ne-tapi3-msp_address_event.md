---
UID: NE:tapi3.__MIDL___MIDL_itf_tapi3_0000_0018_0001
title: MSP_ADDRESS_EVENT
author: windows-sdk-content
description: The MSP_ADDRESS_EVENT constant is returned within the MSP_EVENT_INFO struct by the GetEvent method when MSP_EVENT is ME_ADDRESS_EVENT.
old-location: tapi3\msp_address_event.htm
tech.root: tapi
ms.assetid: 35aecd05-badd-4509-92e5-1936ca075c37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADDRESS_TERMINAL_AVAILABLE, ADDRESS_TERMINAL_UNAVAILABLE, MSP_ADDRESS_EVENT, MSP_ADDRESS_EVENT enumeration [TAPI 2.2], _tapi3_msp_address_event, msp/ADDRESS_TERMINAL_AVAILABLE, msp/ADDRESS_TERMINAL_UNAVAILABLE, msp/MSP_ADDRESS_EVENT, tapi3.msp_address_event
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - MSP_ADDRESS_EVENT
product: Windows
targetos: Windows
req.typenames: MSP_ADDRESS_EVENT
req.redist: 
---

# MSP_ADDRESS_EVENT enumeration


## -description


The <b>MSP_ADDRESS_EVENT</b> constant is returned within the 
<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a> struct by the 
<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">GetEvent</a> method when 
<a href="https://msdn.microsoft.com/53e19eff-b5f0-43fd-b59b-e85e75220282">MSP_EVENT</a> is ME_ADDRESS_EVENT.


## -enum-fields




### -field ADDRESS_TERMINAL_AVAILABLE

A new terminal arrived by PNP.


### -field ADDRESS_TERMINAL_UNAVAILABLE

A terminal has been removed by PNP.


## -see-also




<a href="https://msdn.microsoft.com/df5263f2-9d76-472d-b7fc-724d36f0b58f">ITMSPAddress::GetEvent</a>



<a href="https://msdn.microsoft.com/53e19eff-b5f0-43fd-b59b-e85e75220282">MSP_EVENT</a>



<a href="https://msdn.microsoft.com/5286fbe6-3553-42f1-82e6-5bb6f75f3305">MSP_EVENT_INFO</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 


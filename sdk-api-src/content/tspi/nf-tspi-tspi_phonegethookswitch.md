---
UID: NF:tspi.TSPI_phoneGetHookSwitch
title: TSPI_phoneGetHookSwitch function
author: windows-sdk-content
description: The TSPI_phoneGetHookSwitch function returns the current hookswitch mode of the specified open phone device.
old-location: tspi\tspi_phonegethookswitch.htm
old-project: tapi
ms.assetid: 31248a74-84f2-4ca6-a6fc-f8710953ce34
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: TSPI_phoneGetHookSwitch, TSPI_phoneGetHookSwitch function [TAPI 2.2], _tspi_tspi_phonegethookswitch, tspi.tspi_phonegethookswitch, tspi/TSPI_phoneGetHookSwitch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tspi.h
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
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneGetHookSwitch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_phoneGetHookSwitch function


## -description


The 
<b>TSPI_phoneGetHookSwitch</b> function returns the current hookswitch mode of the specified open phone device.


## -parameters




### -param hdPhone

The service provider's opaque handle to the phone whose hookswitch mode is to be retrieved.


### -param lpdwHookSwitchDevs

A pointer to a <b>DWORD</b>-sized location into which the service provider writes the mode of the phone's hookswitch devices. This parameter uses one of the 
<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ constants</a>. If a bit position is <b>FALSE</b>, the corresponding hookswitch device is onhook. If <b>TRUE</b>, the microphone and/or speaker part of the corresponding hookswitch device is offhook. To find out whether microphone and/or speaker are enabled, TAPI can use 
<a href="https://msdn.microsoft.com/92cf7299-2e1f-42ce-abf7-2824d993bd59">TSPI_phoneGetStatus</a>.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPHONESTATE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.




## -remarks



After the hookswitch state of a device changes, and if hookswitch monitoring is enabled, TAPI is sent a PHONE_STATE message.




## -see-also




<a href="https://msdn.microsoft.com/b3272a75-87b0-4afc-b2e2-2d65e4b49300">PHONEHOOKSWITCHDEV_ Constants</a>



<a href="https://msdn.microsoft.com/798a6c57-d3d3-4924-a925-059de350d18e">PHONESTATUS</a>



<a href="https://msdn.microsoft.com/4772e24c-cafb-4fda-8243-5117c9a73753">PHONE_STATE</a>



<a href="https://msdn.microsoft.com/92cf7299-2e1f-42ce-abf7-2824d993bd59">TSPI_phoneGetStatus</a>



<a href="https://msdn.microsoft.com/e0cfe1b7-9904-4baf-8801-43bc1a5d05d8">TSPI_phoneSetHookSwitch</a>
 

 


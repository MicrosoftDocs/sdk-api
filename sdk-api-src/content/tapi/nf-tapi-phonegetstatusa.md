---
UID: NF:tapi.phoneGetStatusA
title: phoneGetStatusA function
author: windows-sdk-content
description: The phoneGetStatus function enables an application to query the specified open phone device for its overall status.
old-location: tapi2\phonegetstatus.htm
tech.root: Tapi
ms.assetid: d2e9e209-54f5-4895-b57a-a5f4c24e063e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_tapi2_phonegetstatus, phoneGetStatus, phoneGetStatus function [TAPI 2.2], phoneGetStatusA, phoneGetStatusW, tapi/phoneGetStatus, tapi/phoneGetStatusA, tapi/phoneGetStatusW, tapi2.phonegetstatus"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: phoneGetStatusW (Unicode) and phoneGetStatusA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneGetStatus
 - phoneGetStatusA
 - phoneGetStatusW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# phoneGetStatusA function


## -description


The 
<b>phoneGetStatus</b> function enables an application to query the specified open phone device for its overall status.


## -parameters




### -param hPhone

Handle to the open phone device to be queried.


### -param lpPhoneStatus

Pointer to a variably sized data structure of type 
<a href="https://msdn.microsoft.com/798a6c57-d3d3-4924-a925-059de350d18e">PHONESTATUS</a>, which is loaded with the returned information about the phone's status.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_OPERATIONFAILED, PHONEERR_STRUCTURETOOSMALL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.




## -remarks



An application can use this function to determine the current state of an open phone device. The status information describes information about the phone device's hookswitch devices, ringer, volume, display, and lamps.




## -see-also




<a href="https://msdn.microsoft.com/798a6c57-d3d3-4924-a925-059de350d18e">PHONESTATUS</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 


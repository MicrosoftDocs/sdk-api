---
UID: NF:tapi.phoneGetStatusW
title: phoneGetStatusW function (tapi.h)
description: The phoneGetStatus function enables an application to query the specified open phone device for its overall status.helpviewer_keywords: ["_tapi2_phonegetstatus","phoneGetStatus","phoneGetStatus function [TAPI 2.2]","phoneGetStatusA","phoneGetStatusW","tapi/phoneGetStatus","tapi/phoneGetStatusA","tapi/phoneGetStatusW","tapi2.phonegetstatus"]
old-location: tapi2\phonegetstatus.htm
tech.root: Tapi
ms.assetid: d2e9e209-54f5-4895-b57a-a5f4c24e063e
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetstatus, phoneGetStatus, phoneGetStatus function [TAPI 2.2], phoneGetStatusA, phoneGetStatusW, tapi/phoneGetStatus, tapi/phoneGetStatusA, tapi/phoneGetStatusW, tapi2.phonegetstatus
f1_keywords:
- tapi/phoneGetStatus
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# phoneGetStatusW function


## -description


The 
<b>phoneGetStatus</b> function enables an application to query the specified open phone device for its overall status.


## -parameters




### -param hPhone

Handle to the open phone device to be queried.


### -param lpPhoneStatus

Pointer to a variably sized data structure of type 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a>, which is loaded with the returned information about the phone's status.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_OPERATIONFAILED, PHONEERR_STRUCTURETOOSMALL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.




## -remarks



An application can use this function to determine the current state of an open phone device. The status information describes information about the phone device's hookswitch devices, ringer, volume, display, and lamps.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
 

 


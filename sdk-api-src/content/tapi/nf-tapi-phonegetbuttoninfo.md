---
UID: NF:tapi.phoneGetButtonInfo
title: phoneGetButtonInfo function (tapi.h)
description: The phoneGetButtonInfo function returns information about the specified button.
helpviewer_keywords: ["_tapi2_phonegetbuttoninfo","phoneGetButtonInfo","phoneGetButtonInfo function [TAPI 2.2]","phoneGetButtonInfoA","phoneGetButtonInfoW","tapi/phoneGetButtonInfo","tapi/phoneGetButtonInfoA","tapi/phoneGetButtonInfoW","tapi2.phonegetbuttoninfo"]
old-location: tapi2\phonegetbuttoninfo.htm
tech.root: tapi3
ms.assetid: a4df5ba0-7fce-4d29-80a6-4f8f58ae1a83
ms.date: 12/05/2018
ms.keywords: _tapi2_phonegetbuttoninfo, phoneGetButtonInfo, phoneGetButtonInfo function [TAPI 2.2], phoneGetButtonInfoA, phoneGetButtonInfoW, tapi/phoneGetButtonInfo, tapi/phoneGetButtonInfoA, tapi/phoneGetButtonInfoW, tapi2.phonegetbuttoninfo
f1_keywords:
- tapi/phoneGetButtonInfo
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
req.unicode-ansi: phoneGetButtonInfoW (Unicode) and phoneGetButtonInfoA (ANSI)
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
- phoneGetButtonInfo
- phoneGetButtonInfoA
- phoneGetButtonInfoW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# phoneGetButtonInfo function


## -description


The 
<b>phoneGetButtonInfo</b> function returns information about the specified button.


## -parameters




### -param hPhone

Handle to the open phone device.


### -param dwButtonLampID

Button on the phone device.


### -param lpButtonInfo

Pointer to a variably sized structure of type 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>. This data structure describes the mode and the function, and provides additional descriptive text corresponding to the button.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALBUTTONLAMPID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALPHONESTATE, PHONEERR_STRUCTURETOOSMALL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-phonebuttoninfo">PHONEBUTTONINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
 

 


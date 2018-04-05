---
UID: NF:tapi.phoneGetDevCapsA
title: phoneGetDevCapsA function
author: windows-driver-content
description: The phoneGetDevCaps function queries a specified phone device to determine its telephony capabilities.
old-location: tapi2\phonegetdevcaps.htm
old-project: Tapi
ms.assetid: 7bfef6d7-d5fd-4887-afb8-b1d850df050d
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "_tapi2_phonegetdevcaps, phoneGetDevCaps, phoneGetDevCaps function [TAPI 2.2], phoneGetDevCapsA, phoneGetDevCapsW, tapi/phoneGetDevCaps, tapi/phoneGetDevCapsA, tapi/phoneGetDevCapsW, tapi2.phonegetdevcaps"
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
req.unicode-ansi: phoneGetDevCapsW (Unicode) and phoneGetDevCapsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	phoneGetDevCaps
-	phoneGetDevCapsA
-	phoneGetDevCapsW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneGetDevCapsA function


## -description


The 
<b>phoneGetDevCaps</b> function queries a specified phone device to determine its telephony capabilities.


## -parameters




### -param hPhoneApp

Handle to the application's registration with TAPI.


### -param dwDeviceID

Identifier of the phone device to be queried.


### -param dwAPIVersion

Version number of the Telephony API to be used. The high-order word contains the major version number; the low-order word contains the minor version number. This number is obtained with the function 
<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a>.


### -param dwExtVersion

Version number of the service provider-specific extensions to be used. This number is obtained with the function 
<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a>. It can be left zero if no device-specific extensions are to be used. Otherwise, the high-order word contains the major version number; the low-order word contains the minor version number.


### -param lpPhoneCaps

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>. Upon successful completion of the request, this structure is filled with phone device capabilities information.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_INVALPOINTER, PHONEERR_BADDEVICEID, PHONEERR_OPERATIONFAILED, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_OPERATIONUNAVAIL, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_NOMEM, PHONEERR_STRUCTURETOOSMALL, PHONEERR_RESOURCEUNAVAIL, PHONEERR_NODRIVER, PHONEERR_UNINITIALIZED, PHONEERR_NODEVICE.




## -remarks



Before using 
<b>phoneGetDevCaps</b>, the application must negotiate the TAPI version number to use (see 
<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a>) and, optionally, the extension version to use (see 
<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a>).

TAPI and extension version numbers are those under which TAPI, Telephony DLL, and service provider must operate. If version ranges do not overlap, the application and API or service-provider versions are incompatible and an error is returned.




## -see-also




<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/50c2c15c-459f-451b-9b79-9118acc81c8c">phoneNegotiateAPIVersion</a>



<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a>
 

 


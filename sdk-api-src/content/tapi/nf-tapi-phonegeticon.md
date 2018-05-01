---
UID: NF:tapi.phoneGetIcon
title: phoneGetIcon function
author: windows-driver-content
description: The phoneGetIcon function allows an application to retrieve a service phone device-specific (or provider-specific) icon that can be displayed to the user.
old-location: tapi2\phonegeticon.htm
old-project: Tapi
ms.assetid: 6c0fa053-387e-4c1f-a972-b7cd42a1ad00
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "_tapi2_phonegeticon, phoneGetIcon, phoneGetIcon function [TAPI 2.2], phoneGetIconA, phoneGetIconW, tapi/phoneGetIcon, tapi/phoneGetIconA, tapi/phoneGetIconW, tapi2.phonegeticon"
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
req.unicode-ansi: phoneGetIconW (Unicode) and phoneGetIconA (ANSI)
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
-	phoneGetIcon
-	phoneGetIconA
-	phoneGetIconW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneGetIcon function


## -description


The 
<b>phoneGetIcon</b> function allows an application to retrieve a service phone device-specific (or provider-specific) icon that can be displayed to the user.


## -parameters




### -param dwDeviceID

Identifier of the phone device whose icon is requested.


### -param lpszDeviceClass

Pointer to a <b>null</b>-terminated string that identifies a device class name. This device class allows the application to select a specific sub-icon applicable to that device class. This parameter is optional and can be left <b>NULL</b> or empty, in which case the highest-level icon associated with the phone device rather than a specified media stream device would be selected.


### -param lphIcon

Pointer to a memory location in which the handle to the icon is returned.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_BADDEVICEID, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALPOINTER, PHONEERR_OPERATIONFAILED, PHONEERR_INVALDEVICECLASS, PHONEERR_UNINITIALIZED, PHONEERR_NOMEM, PHONEERR_NODEVICE.




## -remarks



The 
<b>phoneGetIcon</b> function causes the provider to return a handle (in <i>lphIcon</i>) to an icon resource (obtained from 
<a href="_win32_loadicon_cpp">LoadIcon</a>) associated with the specified phone. The icon handle is for a resource associated with the provider; the application must use 
<a href="_win32_copyicon_cpp">CopyIcon</a> if it wants to reference the icon after the provider is unloaded, which is unlikely to happen as long as the application has the phone open.

The <i>lpszDeviceClass</i> parameter allows the provider to return different icons based on the type of service being referenced by the caller. The permitted strings are the same as for 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a>. For example, if the phone supports the Comm API, passing "COMM" as <i>lpszDeviceClass</i> causes the provider to return an icon related specifically to the Comm device functions of the service provider. The parameters "tapi/phone", "", or <b>NULL</b> can be used to request the icon for the phone service.

For applications using a TAPI version earlier than 2.0, if the provider does not return an icon (whether because the given device class is invalid or the provider does not support icons), TAPI substitutes a generic  Telephony phone device icon. For applications using TAPI version 2.0 or later, TAPI substitutes the default phone icon only if the <i>lpszDeviceClass</i> parameter is "tapi/phone", "", or <b>NULL</b>. For any other device class, if the given device class is not valid or the provider does not support icons for the class, 
<b>phoneGetIcon</b> returns PHONEERR_INVALDEVICECLASS.




## -see-also




<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a>
 

 


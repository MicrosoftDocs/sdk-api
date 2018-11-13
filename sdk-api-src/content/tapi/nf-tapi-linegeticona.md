---
UID: NF:tapi.lineGetIconA
title: lineGetIconA function
author: windows-sdk-content
description: The lineGetIcon function allows an application to retrieve a service line device-specific (or provider-specific) icon for display to the user.
old-location: tapi2\linegeticon.htm
tech.root: tapi
ms.assetid: 4c76a990-676e-4bb2-b7d7-3b4a0aabf058
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_tapi2_linegeticon, lineGetIcon, lineGetIcon function [TAPI 2.2], lineGetIconA, lineGetIconW, tapi/lineGetIcon, tapi/lineGetIconA, tapi/lineGetIconW, tapi2.linegeticon"
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
req.unicode-ansi: lineGetIconW (Unicode) and lineGetIconA (ANSI)
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
 - lineGetIcon
 - lineGetIconA
 - lineGetIconW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetIconA function


## -description


The 
<b>lineGetIcon</b> function allows an application to retrieve a service line device-specific (or provider-specific) icon for display to the user.


## -parameters




### -param dwDeviceID

Identifier of the line device whose icon is requested.


### -param lpszDeviceClass

Pointer to a <b>null</b>-terminated string that identifies a device class name. This device class allows the application to select a specific sub-icon applicable to that device class. This parameter is optional and can be left <b>NULL</b> or empty, in which case the highest-level icon associated with the line device rather than a specified media stream device would be selected.


### -param lphIcon

Pointer to a memory location in which the handle to the icon is returned.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALDEVICECLASS, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_NODEVICE.




## -remarks



The 
<b>lineGetIcon</b> function causes the provider to return a handle (in <i>lphIcon</i>) to an icon resource (obtained from 
<a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a>) that is associated with the specified line. The icon handle is for a resource associated with the provider. The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms648058(v=VS.85).aspx">CopyIcon</a> if it wants to reference the icon after the provider is unloaded, which is unlikely to happen as long as the application has the line open.

The <i>lpszDeviceClass</i> parameter allows the provider to return different icons based on the type of service being referenced by the caller. The permitted strings are the same as for 
<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>. For example, if the line supports the Comm API, passing "COMM" as <i>lpszDeviceClass</i> causes the provider to return an icon related specifically to the Comm device functions of the service provider. The parameters "tapi/line", "", or <b>NULL</b> can be used to request the icon for the line service.

For applications using an API version earlier than 2.0, if the provider does not return an icon (whether because the given device class is invalid or the provider does not support icons), TAPI substitutes a generic  Telephony line device icon. For applications using API version 2.0 or later, TAPI substitutes the default line icon only if the <i>lpszDeviceClass</i> parameter is "tapi/line", "" or <b>NULL</b>. For any other device class, if the given device class is not valid or the provider does not support icons for the class, 
<b>lineGetIcon</b> returns LINEERR_INVALDEVICECLASS.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/e9981574-0058-420f-9627-6d5a1745a739">lineGetID</a>
 

 


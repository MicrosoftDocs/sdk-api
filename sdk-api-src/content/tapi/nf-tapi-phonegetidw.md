---
UID: NF:tapi.phoneGetIDW
title: phoneGetIDW function
author: windows-sdk-content
description: The phoneGetID function returns a device identifier for the given device class associated with the specified phone device.
old-location: tapi2\phonegetid.htm
old-project: tapi
ms.assetid: 6a9c90ca-7a9e-43de-8075-240185658538
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "_tapi2_phonegetid, phoneGetID, phoneGetID function [TAPI 2.2], phoneGetIDA, phoneGetIDW, tapi/phoneGetID, tapi/phoneGetIDA, tapi/phoneGetIDW, tapi2.phonegetid"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: phoneGetIDW (Unicode) and phoneGetIDA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneGetID
 - phoneGetIDA
 - phoneGetIDW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneGetIDW function


## -description


The 
<b>phoneGetID</b> function returns a device identifier for the given device class associated with the specified phone device.


## -parameters




### -param hPhone

Handle to an open phone device.


### -param lpDeviceID

Pointer to a data structure of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> where the device identifier is returned. Upon successful completion of the request, this location is filled with the device identifier. The format of the returned information depends on the method used by the device class (API) for naming devices.


### -param lpszDeviceClass

Pointer to a null-terminated string that specifies the device class of the device whose identifier is requested. Valid device class strings are those used in the System.ini section to identify device classes.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALDEVICECLASS, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONFAILED, PHONEERR_STRUCTURETOOSMALL, PHONEERR_OPERATIONUNAVAIL.




## -remarks



The 
<b>phoneGetID</b> function can be used to retrieve a phone device identifier given a phone handle. It can also be used to obtain the device identifier of the media device (for device classes such as COM, wave, MIDI, phone, line, or NDIS) associated with the opened phone device. The names of these device class are not case sensitive. This identifier can then be used with the appropriate media API to select the corresponding device.

See 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">TAPI Device Classes</a> for device class names.

A vendor that defines a device-specific media type also needs to define the corresponding device-specific (proprietary) API to manage devices of the media type. To avoid collisions on device class names assigned independently by different vendors, a vendor should select a name that uniquely identifies both the vendor and, following it, the media type. For example: "intel/video".




## -see-also




<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>
 

 


---
UID: NF:tapi.lineGetIDW
title: lineGetIDW function
author: windows-sdk-content
description: The lineGetID function returns a device identifier for the specified device class associated with the selected line, address, or call.
old-location: tapi2\linegetid.htm
old-project: tapi
ms.assetid: e9981574-0058-420f-9627-6d5a1745a739
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: "_tapi2_linegetid, lineGetID, lineGetID function [TAPI 2.2], lineGetIDA, lineGetIDW, tapi/lineGetID, tapi/lineGetIDA, tapi/lineGetIDW, tapi2.linegetid"
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
req.unicode-ansi: lineGetIDW (Unicode) and lineGetIDA (ANSI)
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
 - lineGetID
 - lineGetIDA
 - lineGetIDW
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineGetIDW function


## -description


The 
<b>lineGetID</b> function returns a device identifier for the specified device class associated with the selected line, address, or call.


## -parameters




### -param hLine

Handle to an open line device.


### -param dwAddressID

Address on the given open line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param hCall

Handle to a call.


### -param dwSelect

Specifies whether the requested device identifier is associated with the line, address or a single call. This parameter uses one and only one of the 
<a href="https://msdn.microsoft.com/f19a41bc-403a-4d4b-ab85-240a73514ebb">LINECALLSELECT_ Constants</a>.


### -param lpDeviceID

Pointer to a memory location of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>, where the device identifier is returned. Upon successful completion of the request, this location is filled with the device identifier. The format of the returned information depends on the method used by the device class API for naming devices. Prior to calling 
<b>lineGetID</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

### -param lpszDeviceClass

Pointer to a null-terminated string that specifies the device class of the device whose identifier is requested. Valid device class strings are those used in the SYSTEM.INI section to identify device classes.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSELECT, LINEERR_INVALDEVICECLASS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NODEVICE, LINEERR_UNINITIALIZED.




## -remarks



The 
<b>lineGetID</b> function can be used to retrieve a line-device identifier when given a line handle. This is useful after 
<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a> has been opened using LINEMAPPER as a device identifier in order to determine the real line-device identifier of the opened line. This function can also be used to obtain the device identifier of a phone device or media device (for device classes such as COM, wave, MIDI, phone, line, or NDIS) associated with a call, address or line. This identifier can then be used with the appropriate API (such as phone, MIDI, wave) to select the corresponding media device associated with the specified call.

See 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">TAPI Device Classes</a> for device class names.

A vendor that defines a device-specific media mode also needs to define the corresponding device-specific (proprietary) API to manage devices of the media mode. To avoid collisions on device class names assigned independently by different vendors, a vendor should select a name that uniquely identifies both the vendor and, following it, the media type. For example: "intel/video".




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>



<a href="https://msdn.microsoft.com/7dd39866-0b3e-47be-8aa8-adfb66df6644">lineOpen</a>
 

 


---
UID: NF:tapi.lineGetIDW
title: lineGetIDW function (tapi.h)
description: The lineGetIDW (Unicode) function (tapi.h) returns a device identifier for the specified device class associated with the selected line, address, or call.
helpviewer_keywords: ["_tapi2_linegetid", "lineGetID", "lineGetID function [TAPI 2.2]", "lineGetIDW", "tapi/lineGetID", "tapi/lineGetIDW", "tapi2.linegetid"]
old-location: tapi2\linegetid.htm
tech.root: tapi3
ms.assetid: e9981574-0058-420f-9627-6d5a1745a739
ms.date: 08/09/2022
ms.keywords: _tapi2_linegetid, lineGetID, lineGetID function [TAPI 2.2], lineGetIDA, lineGetIDW, tapi/lineGetID, tapi/lineGetIDA, tapi/lineGetIDW, tapi2.linegetid
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineGetIDW
 - tapi/lineGetIDW
dev_langs:
 - c++
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
<a href="/windows/desktop/Tapi/linecallselect--constants">LINECALLSELECT_ Constants</a>.

### -param lpDeviceID

Pointer to a memory location of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>, where the device identifier is returned. Upon successful completion of the request, this location is filled with the device identifier. The format of the returned information depends on the method used by the device class API for naming devices. Prior to calling 
<b>lineGetID</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

### -param lpszDeviceClass

Pointer to a null-terminated string that specifies the device class of the device whose identifier is requested. Valid device class strings are those used in the SYSTEM.INI section to identify device classes.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_NOMEM, LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCALLSELECT, LINEERR_INVALDEVICECLASS, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NODEVICE, LINEERR_UNINITIALIZED.

## -remarks

The 
<b>lineGetID</b> function can be used to retrieve a line-device identifier when given a line handle. This is useful after 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> has been opened using LINEMAPPER as a device identifier in order to determine the real line-device identifier of the opened line. This function can also be used to obtain the device identifier of a phone device or media device (for device classes such as COM, wave, MIDI, phone, line, or NDIS) associated with a call, address or line. This identifier can then be used with the appropriate API (such as phone, MIDI, wave) to select the corresponding media device associated with the specified call.

See 
<a href="/windows/desktop/Tapi/tapi-device-classes">TAPI Device Classes</a> for device class names.

A vendor that defines a device-specific media mode also needs to define the corresponding device-specific (proprietary) API to manage devices of the media mode. To avoid collisions on device class names assigned independently by different vendors, a vendor should select a name that uniquely identifies both the vendor and, following it, the media type. For example: "intel/video".





> [!NOTE]
> The tapi.h header defines lineGetID as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>

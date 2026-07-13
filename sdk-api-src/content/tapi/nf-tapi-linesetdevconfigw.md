---
UID: NF:tapi.lineSetDevConfigW
title: lineSetDevConfigW function (tapi.h)
description: The lineSetDevConfigW (Unicode) function (tapi.h) allows the application to restore a media stream device's configuration on a line device to a previous setup.
helpviewer_keywords: ["_tapi2_linesetdevconfig", "lineSetDevConfig", "lineSetDevConfig function [TAPI 2.2]", "lineSetDevConfigW", "tapi/lineSetDevConfig", "tapi/lineSetDevConfigW", "tapi2.linesetdevconfig"]
old-location: tapi2\linesetdevconfig.htm
tech.root: tapi3
ms.assetid: f1b04224-e535-4100-b026-3203eebc42c8
ms.date: 08/09/2022
ms.keywords: _tapi2_linesetdevconfig, lineSetDevConfig, lineSetDevConfig function [TAPI 2.2], lineSetDevConfigA, lineSetDevConfigW, tapi/lineSetDevConfig, tapi/lineSetDevConfigA, tapi/lineSetDevConfigW, tapi2.linesetdevconfig
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineSetDevConfigW (Unicode) and lineSetDevConfigA (ANSI)
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
 - lineSetDevConfigW
 - tapi/lineSetDevConfigW
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
 - lineSetDevConfig
 - lineSetDevConfigA
 - lineSetDevConfigW
---

# lineSetDevConfigW function


## -description

The 
<b>lineSetDevConfig</b> function allows the application to restore the configuration of a media stream device on a line device to a setup previously obtained using 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>. For example, the contents of this structure could specify data rate, character format, modulation schemes, and error control protocol settings for a "datamodem" media device associated with the line.

## -parameters

### -param dwDeviceID

Identifier of the line device to be configured.

### -param lpDeviceConfig

Pointer to the opaque configuration data structure that was returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a> in the variable portion of the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure.

### -param dwSize

Number of bytes in the structure pointed to by <i>lpDeviceConfig</i>. This value is returned in the <b>dwStringSize</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure returned by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>.

### -param lpszDeviceClass

Pointer to a null-terminated string that specifies the device class of the device whose configuration is to be set. Valid device class strings are the same as those specified for the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a> function.

## -returns

Returns zero if the function succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NODRIVER, LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALPOINTER, LINEERR_OPERATIONFAILED, LINEERR_INVALPARAM, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALLINESTATE, LINEERR_UNINITIALIZED, LINEERR_NOMEM, LINEERR_NODEVICE.

## -remarks

Call states are device specific.

Typically, an application calls 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a> to identify the media stream device associated with a line, and then calls 
<a href="/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a> to allow the user to set up the device configuration. It could then call 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a> and save the configuration information in a phone book or other database associated with a particular call destination. When the user wants to call the same destination again, this 
<b>lineSetDevConfig</b> function can be used to restore the configuration settings selected by the user. The 
<b>lineSetDevConfig</b>, 
<b>lineConfigDialog</b>, and 
<b>lineGetDevConfig</b> functions can be used, in that order, to allow the user to view and update the settings.

The exact format of the data contained within the structure is specific to the line and media stream API (device class), is undocumented, and is undefined. The application must treat it as "opaque" and not manipulate the contents directly. Generally, the structure can be sent using this function only to the same device from which it was obtained. Certain telephony service providers may, however, permit structures to be interchanged between identical devices (that is, multiple ports on the same multiport modem card). Such interchangeability is not guaranteed in any way, even for devices of the same device class.

Some service providers may permit the configuration to be set while a call is active, and others may not.





> [!NOTE]
> The tapi.h header defines lineSetDevConfig as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevconfig">lineGetDevConfig</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>

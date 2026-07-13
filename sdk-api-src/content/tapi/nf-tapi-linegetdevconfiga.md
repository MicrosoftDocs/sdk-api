---
UID: NF:tapi.lineGetDevConfigA
title: lineGetDevConfigA function (tapi.h)
description: The lineGetDevConfig function returns an &quot;opaque&quot; data structure object, the contents of which are specific to the line (service provider) and device class. (lineGetDevConfigA)
helpviewer_keywords: ["lineGetDevConfigA", "tapi/lineGetDevConfigA"]
old-location: tapi2\linegetdevconfig.htm
tech.root: tapi3
ms.assetid: 39ff5ddb-142e-4f11-9395-e2c3a3ac7d19
ms.date: 12/05/2018
ms.keywords: _tapi2_linegetdevconfig, lineGetDevConfig, lineGetDevConfig function [TAPI 2.2], lineGetDevConfigA, lineGetDevConfigW, tapi/lineGetDevConfig, tapi/lineGetDevConfigA, tapi/lineGetDevConfigW, tapi2.linegetdevconfig
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetDevConfigW (Unicode) and lineGetDevConfigA (ANSI)
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
 - lineGetDevConfigA
 - tapi/lineGetDevConfigA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-tapi32-l1-1-1.dll
 - Tapi32.dll
api_name:
 - lineGetDevConfig
 - lineGetDevConfigA
 - lineGetDevConfigW
---

# lineGetDevConfigA function


## -description

The 
<b>lineGetDevConfig</b> function returns an "opaque" data structure object, the contents of which are specific to the line (service provider) and device class. The data structure object stores the current configuration of a media-stream device associated with the line device.

## -parameters

### -param dwDeviceID

Identifier of the line device to be configured.

### -param lpDeviceConfig

Pointer to the memory location of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> where the device configuration structure is returned. Upon successful completion of the request, this location is filled with the device configuration. The <b>dwStringFormat</b> member in the 
<b>VARSTRING</b> structure is set to STRINGFORMAT_BINARY. Prior to calling 
<b>lineGetDevConfig</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="/windows/desktop/Tapi/memory-allocation">memory allocation</a> topic. </div>
<div> </div>

### -param lpszDeviceClass

Pointer to a null-terminated string that specifies the device class of the device whose configuration is requested. Valid device class 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a> strings are the same as those specified for the function.

## -returns

Returns zero if the function succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NODRIVER, LINEERR_INVALDEVICECLASS, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_NODEVICE.

## -remarks

Call states are device specific.

The 
<b>lineGetDevConfig</b> function can be used to retrieve a data structure from TAPI that specifies the configuration of a media stream device associated with a particular line device. For example, the contents of this structure could specify data rate, character format, modulation schemes, and error control protocol settings for a "datamodem" media device associated with the line.

Typically, an application calls 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a> to identify the media stream device associated with a line, and then calls 
<a href="/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a> to allow the user to set up the device configuration. It could then call 
<b>lineGetDevConfig</b>, and save the configuration information in a phone book (or other database) associated with a particular call destination. When the user later wishes to call the same destination again, 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetdevconfig">lineSetDevConfig</a> can be used to restore the configuration settings selected by the user. The functions 
<b>lineSetDevConfig</b>, 
<b>lineConfigDialog</b>, and 
<b>lineGetDevConfig</b> can be used, in that order, to allow the user to view and update the settings.

The exact format of the data contained within the structure is specific to the line and media stream API (device class), is undocumented, and is undefined. The structure returned by this function cannot be directly accessed or manipulated by the application, but can only be stored intact and later used in 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetdevconfig">lineSetDevConfig</a> to restore the settings. The structure also cannot necessarily be passed to other devices, even of the same device class (although this can work in some instances, it is not guaranteed).





> [!NOTE]
> The tapi.h header defines lineGetDevConfig as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineconfigdialog">lineConfigDialog</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetid">lineGetID</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetdevconfig">lineSetDevConfig</a>

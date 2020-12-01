---
UID: NF:tspi.TSPI_phoneGetID
title: TSPI_phoneGetID function (tspi.h)
description: The TSPI_phoneGetID function returns a device identifier for the given device class associated with the specified phone device.
helpviewer_keywords: ["TSPI_phoneGetID","TSPI_phoneGetID function [TAPI 2.2]","_tspi_tspi_phonegetid","tspi.tspi_phonegetid","tspi/TSPI_phoneGetID"]
old-location: tspi\tspi_phonegetid.htm
tech.root: tapi3
ms.assetid: ed34641d-091a-45a3-becc-b5fca36a9367
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetID, TSPI_phoneGetID function [TAPI 2.2], _tspi_tspi_phonegetid, tspi.tspi_phonegetid, tspi/TSPI_phoneGetID
req.header: tspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_phoneGetID
 - tspi/TSPI_phoneGetID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneGetID
---

# TSPI_phoneGetID function


## -description

The 
<b>TSPI_phoneGetID</b> function returns a device identifier for the given device class associated with the specified phone device.

## -parameters

### -param hdPhone

The handle to the phone to be queried.

### -param lpDeviceID

A pointer to a data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> where the device identifier is returned. The format of the returned information depends on the method used by the device class (API) for naming devices. Prior to calling 
<b>TSPI_phoneGetID</b>, the application sets the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.

### -param lpszDeviceClass

A pointer to a null-terminated Unicode string that specifies the device class of the device whose identifier is requested.

### -param hTargetProcess

The process handle of the application on behalf of which the 
<b>TSPI_phoneGetID</b> function is being invoked. If the information being returned in the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> structure includes a handle for use by the application, the service provider creates or duplicates the handle for the process.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INVALDEVICECLASS, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL.

## -remarks

This operation can be used to retrieve a phone device identifier given a phone handle. It can also be used to obtain the device identifier of the media device (for device classes such as COM, wave, MIDI, phone, line, and mciwave) associated with the opened phone device. This identifier can then be used with the appropriate media API (such as mci, midi, and wav) to select the corresponding device. For more information about common device class names, see 
<a href="/windows/desktop/Tapi/tspi-device-classes">TSPI Device Classes</a>.

The service provider fills in all the members of the 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.

The service provider does not need to be concerned with handling tapi/line and tapi/phone device classes because TAPI handles these for the service provider. Therefore, code for handling these device classes is optional.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>
---
UID: NF:tspi.TSPI_phoneGetIcon
title: TSPI_phoneGetIcon function (tspi.h)
description: The TSPI_phoneGetIcon function retrieves a service phone device-specific (or provider-specific) icon to display to the user.
helpviewer_keywords: ["TSPI_phoneGetIcon","TSPI_phoneGetIcon function [TAPI 2.2]","_tspi_tspi_phonegeticon","tspi.tspi_phonegeticon","tspi/TSPI_phoneGetIcon"]
old-location: tspi\tspi_phonegeticon.htm
tech.root: tapi3
ms.assetid: 765a0f52-9360-4190-abc8-597028f781ac
ms.date: 12/05/2018
ms.keywords: TSPI_phoneGetIcon, TSPI_phoneGetIcon function [TAPI 2.2], _tspi_tspi_phonegeticon, tspi.tspi_phonegeticon, tspi/TSPI_phoneGetIcon
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
 - TSPI_phoneGetIcon
 - tspi/TSPI_phoneGetIcon
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
 - TSPI_phoneGetIcon
---

# TSPI_phoneGetIcon function


## -description

The 
<b>TSPI_phoneGetIcon</b> function retrieves a service phone device-specific (or provider-specific) icon to display to the user.

## -parameters

### -param dwDeviceID

The phone device whose icon is requested.

### -param lpszDeviceClass

A pointer to a <b>null</b>-terminated Unicode string that identifies a device class name. This device class allows the caller to select a specific sub icon applicable to that device class. This parameter is optional and can be left <b>NULL</b> or be empty, in which case the highest level icon associated with the phone device rather than a specified media stream device is selected.

### -param lphIcon

A pointer to a memory location in which the handle to the icon is returned.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALDEVICECLASS, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_RESOURCEUNAVAIL.

## -remarks

<b>TSPI_phoneGetIcon</b> causes the provider to return a handle (in the <b>DWORD</b> pointed to by <i>lphIcon</i>) to an icon resource (obtained from the  
<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a> function) associated with the specified phone. The icon handle is for a resource associated with the provider.

The <i>lpszDeviceClass</i> parameter allows the provider to return different icons based on the type of service being referenced by the caller. The permitted strings are the same as for 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetid">TSPI_phoneGetID</a>. For example, if the phone supports the Comm API, passing comm/datamodem as <i>lpszDeviceClass</i> causes the provider to return an icon related specifically to the Comm device functions of the service provider. For more information about common device classes, see 
<a href="/windows/desktop/Tapi/tspi-device-classes">TSPI Device Classes</a>.

The parameters "tapi/phone", "", or <b>NULL</b> can be used to request the icon for the phone device. A provider can choose to support many icons (selected by <i>lpszDeviceClass</i> and/or phone number), a single icon (such as for the manufacturer, which would be returned for all <i>phoneGetIcon</i> requests regardless of the <i>lpszDeviceClass</i> selected), or no icons, in which case it sets the <b>DWORD</b> pointed to by <i>lphIcon</i> to <b>NULL</b>. TAPI examines the handle returned by the provider, and if the provider returns <b>NULL</b>, TAPI substitutes a generic  Telephony icon included as a resource in TAPI (the generic phone icon).

If the service provider supports no icons, it can leave this function unimplemented, in which case TAPI provides a generic phone icon for the application.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phoneconfigdialog">TSPI_phoneConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetid">TSPI_phoneGetID</a>
---
UID: NF:tspi.TSPI_lineGetDevConfig
title: TSPI_lineGetDevConfig function (tspi.h)
description: The TSPI_lineGetDevConfig function returns a data structure object, the contents of which are specific to the line (service provider) and device class, giving the current configuration of a device associated one-to-one with the line device.
helpviewer_keywords: ["TSPI_lineGetDevConfig","TSPI_lineGetDevConfig function [TAPI 2.2]","_tspi_tspi_linegetdevconfig","tspi.tspi_linegetdevconfig","tspi/TSPI_lineGetDevConfig"]
old-location: tspi\tspi_linegetdevconfig.htm
tech.root: tapi3
ms.assetid: 87307bc6-0c0e-41d0-bc88-2d806214c13e
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetDevConfig, TSPI_lineGetDevConfig function [TAPI 2.2], _tspi_tspi_linegetdevconfig, tspi.tspi_linegetdevconfig, tspi/TSPI_lineGetDevConfig
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
 - TSPI_lineGetDevConfig
 - tspi/TSPI_lineGetDevConfig
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
 - TSPI_lineGetDevConfig
---

# TSPI_lineGetDevConfig function


## -description

The 
<b>TSPI_lineGetDevConfig</b> function returns a data structure object, the contents of which are specific to the line (service provider) and device class, giving the current configuration of a device associated one-to-one with the line device.

## -parameters

### -param dwDeviceID

The line device to be configured.

### -param lpDeviceConfig

A pointer to a data structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a> where the device configuration structure of the associated device is returned. Upon successful completion of the request, the service provider fills this data structure with the device configuration. The <b>dwStringFormat</b> member in the 
<b>VARSTRING</b> structure must be set to STRINGFORMAT_BINARY. If the <b>dwTotalSize</b> member of the 
<b>VARSTRING</b> structure pointed to by the <i>lpDeviceConfig</i> parameter is greater than or equal to the size of the fixed portion of the structure, the service provider sets the <b>dwNeededSize</b> member to the required size and returns zero.

### -param lpszDeviceClass

A pointer to a null-terminated Unicode string that specifies the device class of the device whose configuration is requested. Valid device class strings are the same as those specified for the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a> function when it is applied to a line device (<i>dwSelect</i> has the value LINECALLSELECT_LINE).

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALDEVICECLASS, LINEERR_NOMEM, LINEERR_INVALPOINTER, LINEERR_OPERATIONUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_OPERATIONFAILED, LINEERR_NODRIVER, LINEERR_RESOURCEUNAVAIL.

## -remarks

The call state is device-specific.

This function can be used to retrieve a data structure from the service provider that specifies the configuration of a device associated one-to-one with the line device. The <i>lpszDeviceClass</i> parameter selects which of among possibly several different classes of devices is to have its configuration retrieved. The set of supported classes is restricted to those whose devices correspond one-to-one with the line device. For more information about common device classes, see 
<a href="/windows/desktop/Tapi/tspi-device-classes">TSPI Device Classes</a>.

A service provider should typically allow the tapi/line device class under this function. It would retrieve parameters that have "line" scope, such as the list of addresses in this line, the list of physical hardware devices such as COMM ports corresponding to the addresses, maximum number of concurrent calls (if configurable), and so on.

In general, this function does not allow media-related device classes such as mci waveaudio, low level wave, or datamodem device classes, because these usually apply to a particular call or a particular address. Because there can be more than one of these per line device, the identification of the particular call or address simply by the line device identifier parameter in this function would be ambiguous. An exception can be made for call-specific or address-specific device classes in cases where there is class configuration information that applies to the entire line device scope, such as initial defaults, and so on.

There are several reasons why exceptional support for call-specific and address-specific device classes is of only limited value under this function. First, because these classes can be ambiguous on multiple-address/multiple-call service providers, only a subset of service providers support them. Applications are not likely to add a device-specific dependency on the inclusion of these classes in this function. Second, as higher-level media "classes" emerge that implement high-level protocols such as dial-in file system access in terms of low-level transport APIs, configuration for these classes tends toward "instance" scope instead of "class" scope. The high-level media API must supply its own functions to configure call-specific or address-specific instances.

Whatever sort of devices and device classes this function supports, it can potentially affect two kinds of configuration information: permanent and temporary. Permanent information survives across different "opens" of the line, and even across different "inits" of the service provider itself. Temporary information survives only within a unique "open" of the line. When the line is closed, any such temporary information that has been retrieved or set through 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a> can revert to default or undefined values. The caller can reliably retrieve any temporary configuration only by a sequence such as 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineopen">TSPI_lineOpen</a>, 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconfigdialog">TSPI_lineConfigDialog</a>, 
<b>TSPI_lineGetDevConfig</b>. The caller can reliably set temporary configuration information retrieved by such a sequence through a sequence such as 
<b>TSPI_lineOpen</b>, 
<b>TSPI_lineSetDevConfig</b>. The temporary part of configuration remains stable only until the next 
<b>TSPI_lineConfigDialog</b>, 
<b>TSPI_lineSetDevConfig</b>, or 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclose">TSPI_lineClose</a>. The service provider must take care of storing any permanent part of the configuration, typically in an .ini file, and reloading it whenever the service provider is initialized.

The exact format of the data contained within the structure returned by this function is specific to the line and device class API, is undocumented, and is undefined. The structure returned by this function cannot be directly accessed or manipulated by the application, but can only be stored intact and later used in 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a> to restore the settings. The structure also cannot necessarily be passed to other devices, even of the same device class (although this may work in some instances, it is not guaranteed). A service provider should put items in the data structure to allow it to be checked for consistency to guard against failures due to a client application passing incompatible information.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineclose">TSPI_lineClose</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconfigdialog">TSPI_lineConfigDialog</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetid">TSPI_lineGetID</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineopen">TSPI_lineOpen</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdevconfig">TSPI_lineSetDevConfig</a>



<a href="/windows/desktop/api/tapi/ns-tapi-varstring">VARSTRING</a>
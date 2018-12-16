---
UID: NF:tspi.TSPI_lineSetDevConfig
title: TSPI_lineSetDevConfig function
author: windows-sdk-content
description: The TSPI_lineSetDevConfig function restores the configuration of a device associated one-to-one with the line device from a data structure previously obtained using TSPI_lineGetDevConfig.
old-location: tspi\tspi_linesetdevconfig.htm
tech.root: tapi
ms.assetid: 41699ca8-a30d-48ab-bace-bc2b95b67e77
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_lineSetDevConfig, TSPI_lineSetDevConfig function [TAPI 2.2], _tspi_tspi_linesetdevconfig, tspi.tspi_linesetdevconfig, tspi/TSPI_lineSetDevConfig
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetDevConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineSetDevConfig function


## -description


The 
<b>TSPI_lineSetDevConfig</b> function restores the configuration of a device associated one-to-one with the line device from a data structure previously obtained using 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a>. The contents of this data structure are specific to the line [service provider] and device class.


## -parameters




### -param dwDeviceID

The line device to be configured.


### -param lpDeviceConfig

A pointer to the configuration data structure that is returned in the variable portion of the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure by 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a>.


### -param dwSize

The number of bytes in the structure pointed to by <i>lpDeviceConfig</i>. This value is returned in the <b>dwStringSize</b> member in the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure returned by 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a>. 




<div class="alert"><b>Note</b>  If the size parameters in the structure are not correct, there is a possibility that data could get overwritten. For more information on setting structure sizes, see the 
<a href="https://msdn.microsoft.com/61313fe3-74a1-4195-b5af-37463dad02c1">memory allocation</a> topic. </div>
<div> </div>

### -param lpszDeviceClass

A pointer to a null-terminated Unicode string that specifies the device class of the device whose configuration is to be restored. Valid device class strings are the same as those specified for the 
<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a> function when it is applied to a "line" device (that is, when <i>dwSelect</i> has the value LINECALLSELECT_LINE).


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are:

LINEERR_INVALDEVICECLASS, LINEERR_NOMEM, LINEERR_INVALPOINTER, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALPARAM, LINEERR_OPERATIONFAILED, LINEERR_INVALLINESTATE, LINEERR_RESOURCEUNAVAIL, LINEERR_NODRIVER.




## -remarks



The call state is device specific.

The service provider returns LINEERR_INVALPARAM if the information contained in the structure pointed to by <i>lpDeviceConfig</i> is not valid for this device.

The service provider returns LINEERR_INVALLINESTATE if the device configuration cannot be changed in the current line state. The line may be in use by another application.

This function can be used to restore the configuration of a device associated one-to-one with the line device from a data structure previously retrieved from the service provider using the 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a> function. The <i>lpszDeviceClass</i> parameter selects which of among possibly several different classes of devices is to have its configuration restored. The set of supported classes is restricted to those whose devices correspond one-to-one with the line device. For more information about common device classes, see 
<a href="https://msdn.microsoft.com/b29ea789-d017-4e35-b77a-c0d54ac54c66">TSPI Device Classes</a>.

A service provider typically allows the tapi/line device class under this function. It restores parameters that have "line" scope, such as the list of addresses in this line and the list of physical hardware devices such as COMM ports corresponding to the addresses or the maximum number of concurrent calls (if configurable).

In general, this function does NOT allow media-related device classes such as mci waveaudio, low level wave, or datamodem device classes, because these usually apply to a particular call or a particular address. Because there can be more than one of these per line device, the identification of the particular call or address simply by the line device identifier parameter in this function is ambiguous. An exception can be made for call-specific or address-specific device classes in cases where there is class configuration information that applies to the entire line device scope, such as initial defaults.

There are several reasons why exceptional support for call-specific and address-specific device classes is of only limited value under this function. First, because these classes can be ambiguous on multiple-address, multiple-call service providers, only a subset of service providers support them. Application programs are not likely to add a device-specific dependency on the inclusion of these classes in this function. Second, as higher-level media classes emerge that implement high-level protocols such as dial-in file system access in terms of low-level transport APIs, configuration for these classes tends toward instance scope instead of class scope. The high-level media API has to supply its own functions to configure call-specific or address-specific instances.

Whatever sort of devices and device classes this function supports, it can potentially affect two kinds of configuration information: permanent and temporary. Permanent information survives across different "opens" of the line, and even across different "inits" of the service provider itself. Temporary information survives only within a unique "open" of the line. When the line is closed, any such temporary information that has been set or retrieved through 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a> can revert to default or undefined values. The caller can reliably retrieve any temporary configuration only by a sequence such as 
<a href="https://msdn.microsoft.com/97cde843-65bc-46ae-a6ae-724f2c9c5217">TSPI_lineOpen</a>, 
<a href="https://msdn.microsoft.com/b0f26029-ddb2-472c-8a09-2abf213dab16">TSPI_lineConfigDialog</a>, 
<b>TSPI_lineGetDevConfig</b>. The caller can reliably set temporary configuration information retrieved by such a sequence through a sequence such as 
<b>TSPI_lineOpen</b>, 
<b>TSPI_lineSetDevConfig</b>. The temporary part of configuration remains stable only until the next 
<b>TSPI_lineConfigDialog</b>, 
<b>TSPI_lineSetDevConfig</b>, or 
<a href="https://msdn.microsoft.com/d1041620-609b-476b-bdb7-e1e0cebd74f1">TSPI_lineClose</a>. The service provider must take care of storing any permanent part of the configuration, typically in an .ini file, and reloading it whenever the service provider is initialized.

The exact format of the data contained within the structure passed to this function is specific to the line and device class API, is undocumented, and is undefined. The structure passed to this function cannot be directly accessed or manipulated by the application, but can only be stored intact and later used from a previous 
<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a> to obtain the settings. The structure also cannot necessarily be passed to other devices, even of the same device class (although this may work in some instances, it is not guaranteed). A service provider should check this data structure for consistency to guard against failures due to a client application passing incompatible information.

<div class="alert"><b>Note</b>  Some service providers may permit the configuration to be set while a device is in use, and others may not.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d1041620-609b-476b-bdb7-e1e0cebd74f1">TSPI_lineClose</a>



<a href="https://msdn.microsoft.com/b0f26029-ddb2-472c-8a09-2abf213dab16">TSPI_lineConfigDialog</a>



<a href="https://msdn.microsoft.com/87307bc6-0c0e-41d0-bc88-2d806214c13e">TSPI_lineGetDevConfig</a>



<a href="https://msdn.microsoft.com/d4331721-61c3-4de0-bb1f-c27f475170d1">TSPI_lineGetID</a>



<a href="https://msdn.microsoft.com/97cde843-65bc-46ae-a6ae-724f2c9c5217">TSPI_lineOpen</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>
 

 


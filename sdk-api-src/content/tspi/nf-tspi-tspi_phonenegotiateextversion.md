---
UID: NF:tspi.TSPI_phoneNegotiateExtVersion
title: TSPI_phoneNegotiateExtVersion function
author: windows-sdk-content
description: The TSPI_phoneNegotiateExtVersion function returns the highest extension version number the service provider can operate under for this device, given the range of possible extension versions.
old-location: tspi\tspi_phonenegotiateextversion.htm
old-project: tapi
ms.assetid: 03ea6d25-8e65-4c8a-80dc-f2ecd214ad0e
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: TSPI_phoneNegotiateExtVersion, TSPI_phoneNegotiateExtVersion function [TAPI 2.2], _tspi_tspi_phonenegotiateextversion, tspi.tspi_phonenegotiateextversion, tspi/TSPI_phoneNegotiateExtVersion
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_phoneNegotiateExtVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_phoneNegotiateExtVersion function


## -description


The 
<b>TSPI_phoneNegotiateExtVersion</b> function returns the highest extension version number the service provider can operate under for this device, given the range of possible extension versions.


## -parameters




### -param dwDeviceID

Identifies the phone device for which interface version negotiation is to be performed.


### -param dwTSPIVersion

Specifies an interface version number that is negotiated for this device using 
<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a>. This function operates according to the interface specification at this version level.


### -param dwLowVersion

The lowest extension version number under which TAPI or its client application can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number.


### -param dwHighVersion

The highest extension version number under which TAPI or its client application can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number.


### -param lpdwExtVersion

A pointer to a <b>DWORD</b>. Upon a successful return from this function, the service provider fills this location with the highest extension version number, within the range requested by the caller, under which the service provider can operate. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. If the requested range does not overlap the range supported by the service provider, the function returns PHONEERR_INCOMPATIBLEEXTVERSION.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_OPERATIONFAILED, PHONEERR_NODRIVER, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NOMEM.




## -remarks



This function can be called before or after the device has been opened by TAPI. If the device is currently open and has an extension version selected, the function should return that version number if it is within the requested range. If the selected version number is outside the requested range, the function returns PHONEERR_INCOMPATIBLEEXTVERSION.




## -see-also




<a href="https://msdn.microsoft.com/a6bca1a3-a6cd-4cb5-80e9-0da0ad6ba8dc">TSPI_phoneNegotiateTSPIVersion</a>
 

 


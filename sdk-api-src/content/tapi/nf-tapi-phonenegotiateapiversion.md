---
UID: NF:tapi.phoneNegotiateAPIVersion
title: phoneNegotiateAPIVersion function
author: windows-sdk-content
description: The phoneNegotiateAPIVersion allows an application to negotiate an API version to use for the specified phone device.
old-location: tapi2\phonenegotiateapiversion.htm
tech.root: tapi
ms.assetid: 50c2c15c-459f-451b-9b79-9118acc81c8c
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_phonenegotiateapiversion, phoneNegotiateAPIVersion, phoneNegotiateAPIVersion function [TAPI 2.2], tapi/phoneNegotiateAPIVersion, tapi2.phonenegotiateapiversion"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneNegotiateAPIVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# phoneNegotiateAPIVersion function


## -description


The 
<b>phoneNegotiateAPIVersion</b> allows an application to negotiate an API version to use for the specified phone device.


## -parameters




### -param hPhoneApp

Handle to the application's registration with TAPI.


### -param dwDeviceID

Identifier of the phone device to be queried.


### -param dwAPILowVersion

Least recent API version the application is compliant with. The high-order word is the major version number, the low-order word is the minor version number.


### -param dwAPIHighVersion

Most recent API version the application is compliant with. The high-order word is the major version number, the low-order word is the minor version number.


### -param lpdwAPIVersion

Pointer to a <b>DWORD</b> in which the API version number that was negotiated will be returned. If negotiation succeeds, this number is in the range <i>dwAPILowVersion</i> to <i>dwAPIHighVersion</i>.


### -param lpExtensionID

Pointer to a structure of type 
<a href="https://msdn.microsoft.com/61f376fd-2287-4425-9445-163f71aebf04">PHONEEXTENSIONID</a>. If the service provider for the specified <i>dwDeviceID</i> parameter supports provider-specific extensions, this structure is filled with the extension identifier of these extensions when negotiation succeeds. This structure contains all zeros if the line provides no extensions. An application can ignore the returned parameter if it does not use extensions.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_BADDEVICEID, PHONEERR_OPERATIONUNAVAIL, PHONEERR_NODRIVER, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_INCOMPATIBLEAPIVERSION, PHONEERR_UNINITIALIZED, PHONEERR_NODEVICE.




## -remarks



The 
<b>phoneNegotiateAPIVersion</b> function is used to negotiate the API version number to use with the specified phone device. It returns the extension identifier supported by the phone device, or zeros if no extensions are provided.

If the application wants to use the extensions defined by the returned extension identifier, it must call 
<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a> to negotiate the extension version to use.

Use 
<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a> to determine the number of phone devices present in the system. The device identifier specified by <i>dwDeviceID</i> varies from zero to one less than the number of phone devices present.

The API version number negotiated is that under which TAPI can operate. If version ranges do not overlap, the application, API, or service-provider versions are incompatible and an error is returned.




## -see-also




<a href="https://msdn.microsoft.com/61f376fd-2287-4425-9445-163f71aebf04">PHONEEXTENSIONID</a>



<a href="https://msdn.microsoft.com/0d1a81d2-aa9e-4a85-85d3-aa4eabb26eb5">Supplementary Phone Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/35fea8f9-307e-4429-b4ec-ffb5c62c2610">TAPI Versioning</a>



<a href="https://msdn.microsoft.com/362e37df-4b14-4651-8d23-b70613e354c8">phoneInitializeEx</a>



<a href="https://msdn.microsoft.com/f62aa1da-7256-400a-998d-4c24d01989ec">phoneNegotiateExtVersion</a>
 

 


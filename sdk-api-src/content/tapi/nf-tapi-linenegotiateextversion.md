---
UID: NF:tapi.lineNegotiateExtVersion
title: lineNegotiateExtVersion function
author: windows-sdk-content
description: The lineNegotiateExtVersion function allows an application to negotiate an extension version to use with the specified line device. This operation need not be called if the application does not support extensions.
old-location: tapi2\linenegotiateextversion.htm
old-project: tapi
ms.assetid: 89a49709-a15b-4358-984a-fd836d8e237b
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: "_tapi2_linenegotiateextversion, lineNegotiateExtVersion, lineNegotiateExtVersion function [TAPI 2.2], tapi/lineNegotiateExtVersion, tapi2.linenegotiateextversion"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tapi.h
req.include-header: 
req.redist: 
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
req.typenames: FLICK_POINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineNegotiateExtVersion
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineNegotiateExtVersion function


## -description


The 
<b>lineNegotiateExtVersion</b> function allows an application to negotiate an extension version to use with the specified line device. This operation need not be called if the application does not support extensions.


## -parameters




### -param hLineApp

Handle to the application's registration with TAPI.


### -param dwDeviceID

Identifier of the line device to be queried.


### -param dwAPIVersion

TAPI version number that was negotiated for the specified line device using 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>.


### -param dwExtLowVersion

Earliest extension version of the extension identifier returned by 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> with which the application is compliant. The high-order word is the major version number; the low-order word is the minor version number.


### -param dwExtHighVersion

Latest extension version of the extension identifier returned by 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> with which the application is compliant. The high-order word is the major version number; the low-order word is the minor version number.


### -param lpdwExtVersion

Pointer to a variable that contains the extension version number that was negotiated. If negotiation succeeds, this number is in the range between <i>dwExtLowVersion</i> and <i>dwExtHighVersion</i>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_BADDEVICEID, LINEERR_NOMEM, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_NODRIVER, LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_OPERATIONFAILED, LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NODEVICE, LINEERR_OPERATIONUNAVAIL.




## -remarks



Use 
<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a> to determine the number of line devices present in the system. The device identifier specified by <i>dwDeviceID</i> varies from zero to one less than the number of line devices present.

The 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> function negotiates the API version number to use. It also retrieves the extension identifier supported by the line device, which is zeros if no extensions are provided. Version numbers should be incremented by one for each release. Leaving gaps in release version numbering can cause unexpected results.

If the application wants to use the extensions defined by the returned extension identifier, it must call 
<b>lineNegotiateExtVersion</b> to negotiate the extension version to use.

The extension version number negotiated is that under which the application and service provider must both operate. If version ranges do not overlap, the application and service provider versions are incompatible and an error is returned.




## -see-also




<a href="https://msdn.microsoft.com/f16aabf1-c034-4f91-87b2-c98cdf6d67ea">Extended Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/18cd145d-e434-433a-ab10-91bf5b060c21">lineInitializeEx</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 


---
UID: NF:tapi.lineDevSpecific
title: lineDevSpecific function
author: windows-driver-content
description: The lineDevSpecific function enables service providers to provide access to features not offered by other TAPI functions.
old-location: tapi2\linedevspecific.htm
old-project: Tapi
ms.assetid: 28f43b21-5118-465f-95b3-036aab16a049
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "_tapi2_linedevspecific, lineDevSpecific, lineDevSpecific function [TAPI 2.2], tapi/lineDevSpecific, tapi2.linedevspecific"
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineDevSpecific
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineDevSpecific function


## -description


The 
<b>lineDevSpecific</b> function enables service providers to provide access to features not offered by other TAPI functions. The meaning of the extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.


## -parameters




### -param hLine

Handle to a line device. This parameter is required.


### -param dwAddressID

Address identifier on the given line device. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param hCall

Handle to a call. This parameter is optional, but if it is specified, the call it represents must belong to the <i>hLine</i> line device. The call state of <i>hCall</i> is device specific.


### -param lpParams

Pointer to a memory area used to hold a parameter block. The format of this parameter block is device specific and its contents are passed by TAPI to or from the service provider.


### -param dwSize

Size of the parameter block area, in bytes.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds, or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESSID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_UNINITIALIZED, LINEERR_NOMEM.

Additional return values are device specific.




## -remarks



This operation is part of the Extended Telephony services. It provides access to a device-specific feature without defining its meaning. This operation is only available if the application has successfully negotiated a device-specific extension version.

This function provides a generic parameter profile. The interpretation of the parameter structure is device specific. Whether <i>dwAddressID</i> and/or <i>hCall</i> are expected to be valid is device specific. If specified, they must belong to <i>hLine</i>. Indications and replies sent back the application that are device specific should use the 
<a href="https://msdn.microsoft.com/6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc">LINE_DEVSPECIFIC</a> message.

A service provider can provide access to device-specific functions by defining parameters for use with this function. Applications that want to make use of these device-specific extensions should consult the device-specific (in this case, vendor-specific) documentation that describes what extensions are defined. Typically, an application that relies on these device-specific extensions is not able to work with other service provider environments.

<div class="alert"><b>Caution</b>  TAPI will write the returned data to the buffer referenced by lParam when the LINE_REPLY message is returned. This means that the buffer must remain valid until the LINE_REPLY message is returned; otherwise, data corruption and exceptions may occur.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f16aabf1-c034-4f91-87b2-c98cdf6d67ea">Extended Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc">LINE_DEVSPECIFIC</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 


---
UID: NF:tapi.phoneDevSpecific
title: phoneDevSpecific function
author: windows-sdk-content
description: The phoneDevSpecific function is used as a general extension mechanism to enable a Telephony API implementation to provide features not described in the other TAPI functions. The meanings of these extensions are device specific.
old-location: tapi2\phonedevspecific.htm
old-project: Tapi
ms.assetid: 7199b489-bf66-4380-8d1c-73de5aeb7489
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_phonedevspecific, phoneDevSpecific, phoneDevSpecific function [TAPI 2.2], tapi/phoneDevSpecific, tapi2.phonedevspecific"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	phoneDevSpecific
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneDevSpecific function


## -description


The 
<b>phoneDevSpecific</b> function is used as a general extension mechanism to enable a Telephony API implementation to provide features not described in the other TAPI functions. The meanings of these extensions are device specific.


## -parameters




### -param hPhone

Handle to a phone device.


### -param lpParams

Pointer to a memory area used to hold a parameter block. Its interpretation is device specific. The contents of the parameter block are passed unchanged to or from the service provider by TAPI.


### -param dwSize

Size of the parameter block area, in bytes.


## -returns



Returns a positive request identifier if the function is completed asynchronously or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALPHONEHANDLE, PHONEERR_NOMEM, PHONEERR_INVALPOINTER, PHONEERR_RESOURCEUNAVAIL, PHONEERR_OPERATIONUNAVAIL, PHONEERR_UNINITIALIZED, PHONEERR_OPERATIONFAILED.

Additional return values are device specific.




## -remarks



This operation provides a generic parameter profile. The interpretation of the parameter block is device specific. Indications and replies that are device specific should use the 
<a href="https://msdn.microsoft.com/e3e803dd-b041-48b7-9acf-a89989370204">PHONE_DEVSPECIFIC</a> message.

A service provider can provide access to device-specific functions by defining parameters for use with this operation. Applications that want to make use of these device-specific extensions should consult the device-specific (vendor-specific) documentation that describes which extensions are defined. Typically, an application that relies on these device-specific extensions is not portable to work with other service-provider environments.




## -see-also




<a href="https://msdn.microsoft.com/f16aabf1-c034-4f91-87b2-c98cdf6d67ea">Extended Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/e3e803dd-b041-48b7-9acf-a89989370204">PHONE_DEVSPECIFIC</a>



<a href="https://msdn.microsoft.com/434f37d6-f385-4cc9-9658-2b683cab532c">PHONE_REPLY</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 


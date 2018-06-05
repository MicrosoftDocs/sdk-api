---
UID: NF:tapi.lineDevSpecificFeature
title: lineDevSpecificFeature function
author: windows-sdk-content
description: The lineDevSpecificFeature function enables service providers to provide access to features not offered by other TAPI functions.
old-location: tapi2\linedevspecificfeature.htm
old-project: Tapi
ms.assetid: 8498318f-9615-4242-86e2-c57b50293b83
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "_tapi2_linedevspecificfeature, lineDevSpecificFeature, lineDevSpecificFeature function [TAPI 2.2], tapi/lineDevSpecificFeature, tapi2.linedevspecificfeature"
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
-	lineDevSpecificFeature
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineDevSpecificFeature function


## -description


The 
<b>lineDevSpecificFeature</b> function enables service providers to provide access to features not offered by other TAPI functions. The meaning of these extensions are device specific, and taking advantage of these extensions requires the application to be fully aware of them.


## -parameters




### -param hLine

Handle to the line device.


### -param dwFeature

Feature to invoke on the line device. This parameter uses the 
<a href="https://msdn.microsoft.com/33d369d0-2221-403e-8fbc-a9a1cbd640ad">PHONEBUTTONFUNCTION_ Constants</a>.


### -param lpParams

Pointer to a memory area used to hold a feature-dependent parameter block. The format of this parameter block is device specific and its contents are passed through by TAPI to or from the service provider.


### -param dwSize

Size of the buffer, in bytes.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALFEATURE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

Additional return values are device specific.




## -remarks



This operation is part of the Extended Telephony services. It provides access to a device-specific feature without defining its meaning. This operation is only available if the application has successfully negotiated a device-specific extension version.

This function provides the application with phone feature-button emulation capabilities. When an application invokes this operation, it specifies the equivalent of a button-press event. This method of invoking features is device dependent, as TAPI does not define their meaning. Typically, an application that relies on these device-specific extensions does not work with other service provider environments.

The structure pointed to by <i>lpParams</i> should not contain any pointers because they would not be properly translated (thunked) when running a 16-bit application in a 32-bit version of TAPI and vice versa.




## -see-also




<a href="https://msdn.microsoft.com/f16aabf1-c034-4f91-87b2-c98cdf6d67ea">Extended Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 


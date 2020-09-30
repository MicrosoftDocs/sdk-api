---
UID: NF:tapi.lineDevSpecificFeature
title: lineDevSpecificFeature function (tapi.h)
description: The lineDevSpecificFeature function enables service providers to provide access to features not offered by other TAPI functions.
helpviewer_keywords: ["_tapi2_linedevspecificfeature","lineDevSpecificFeature","lineDevSpecificFeature function [TAPI 2.2]","tapi/lineDevSpecificFeature","tapi2.linedevspecificfeature"]
old-location: tapi2\linedevspecificfeature.htm
tech.root: tapi3
ms.assetid: 8498318f-9615-4242-86e2-c57b50293b83
ms.date: 12/05/2018
ms.keywords: _tapi2_linedevspecificfeature, lineDevSpecificFeature, lineDevSpecificFeature function [TAPI 2.2], tapi/lineDevSpecificFeature, tapi2.linedevspecificfeature
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineDevSpecificFeature
 - tapi/lineDevSpecificFeature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineDevSpecificFeature
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
<a href="/windows/desktop/Tapi/phonebuttonfunction--constants">PHONEBUTTONFUNCTION_ Constants</a>.

### -param lpParams

Pointer to a memory area used to hold a feature-dependent parameter block. The format of this parameter block is device specific and its contents are passed through by TAPI to or from the service provider.

### -param dwSize

Size of the buffer, in bytes.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALFEATURE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

Additional return values are device specific.

## -remarks

This operation is part of the Extended Telephony services. It provides access to a device-specific feature without defining its meaning. This operation is only available if the application has successfully negotiated a device-specific extension version.

This function provides the application with phone feature-button emulation capabilities. When an application invokes this operation, it specifies the equivalent of a button-press event. This method of invoking features is device dependent, as TAPI does not define their meaning. Typically, an application that relies on these device-specific extensions does not work with other service provider environments.

The structure pointed to by <i>lpParams</i> should not contain any pointers because they would not be properly translated (thunked) when running a 16-bit application in a 32-bit version of TAPI and vice versa.

## -see-also

<a href="/windows/desktop/Tapi/extended-telephony-services-reference">Extended Telephony Services Reference</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
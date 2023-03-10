---
UID: NF:tapi.lineSetCallQualityOfService
title: lineSetCallQualityOfService function (tapi.h)
description: The lineSetCallQualityOfService function allows the application to attempt to change the quality of service parameters (reserved capacity and performance guarantees) for an existing call.
helpviewer_keywords: ["_tapi2_linesetcallqualityofservice","lineSetCallQualityOfService","lineSetCallQualityOfService function [TAPI 2.2]","tapi/lineSetCallQualityOfService","tapi2.linesetcallqualityofservice"]
old-location: tapi2\linesetcallqualityofservice.htm
tech.root: tapi3
ms.assetid: 6a977dab-70f6-4462-a94f-78acdec7decf
ms.date: 12/05/2018
ms.keywords: _tapi2_linesetcallqualityofservice, lineSetCallQualityOfService, lineSetCallQualityOfService function [TAPI 2.2], tapi/lineSetCallQualityOfService, tapi2.linesetcallqualityofservice
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
 - lineSetCallQualityOfService
 - tapi/lineSetCallQualityOfService
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
 - lineSetCallQualityOfService
---

# lineSetCallQualityOfService function


## -description

The 
<b>lineSetCallQualityOfService</b> function allows the application to attempt to change the quality of service parameters (reserved capacity and performance guarantees) for an existing call. Except for basic parameter validation, this is a straight pass-through to a service provider.

## -parameters

### -param hCall

Handle to the call. The application must have OWNER privilege.

### -param lpSendingFlowspec

Pointer to memory containing a 
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory in the application process, because TAPI will not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.

### -param dwSendingFlowspecSize

Total size of the <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure and accompanying provider-specific data, in bytes. This is equivalent to what would have been stored in <b>SendingFlowspec</b> in a 
<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure.

### -param lpReceivingFlowspec

Pointer to memory containing a <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure must not contain pointers to other blocks of memory in the application process, because TAPI will not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.

### -param dwReceivingFlowspecSize

Total size of the <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> and accompanying provider-specific data, in bytes. This is equivalent to what would have been stored in <b>ReceivingFlowspec</b> in a <a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure.

## -returns

Returns a positive request identifier if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCALLSTATE, LINEERR_INVALPARAM, LINEERR_INVALPOINTER, LINEERR_INVALRATE, LINEERR_NOMEM, LINEERR_NOTOWNER, LINEERR_OPERATIONUNAVAIL, LINEERR_OPERATIONFAILED, LINEERR_RATEUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
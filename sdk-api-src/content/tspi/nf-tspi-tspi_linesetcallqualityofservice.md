---
UID: NF:tspi.TSPI_lineSetCallQualityOfService
title: TSPI_lineSetCallQualityOfService function (tspi.h)
description: The TSPI_lineSetCallQualityOfService function service provider attempts to renegotiate the QOS on the call with the switch If the desired QOS is not available, then the function fails, but the call continues with the previous QOS.
helpviewer_keywords: ["TSPI_lineSetCallQualityOfService","TSPI_lineSetCallQualityOfService function [TAPI 2.2]","_tspi_tspi_linesetcallqualityofservice","tspi.tspi_linesetcallqualityofservice","tspi/TSPI_lineSetCallQualityOfService"]
old-location: tspi\tspi_linesetcallqualityofservice.htm
tech.root: tapi3
ms.assetid: ebef3ee3-94e3-4aef-831d-5ce031882b5c
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetCallQualityOfService, TSPI_lineSetCallQualityOfService function [TAPI 2.2], _tspi_tspi_linesetcallqualityofservice, tspi.tspi_linesetcallqualityofservice, tspi/TSPI_lineSetCallQualityOfService
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
 - TSPI_lineSetCallQualityOfService
 - tspi/TSPI_lineSetCallQualityOfService
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
 - TSPI_lineSetCallQualityOfService
---

# TSPI_lineSetCallQualityOfService function


## -description

The 
<b>TSPI_lineSetCallQualityOfService</b> function service provider attempts to renegotiate the QOS on the call with the switch If the desired QOS is not available, then the function fails, but the call continues with the previous QOS. If the function succeeds, the new QOS information is stored in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>; a LINECALLINFOSTATE_QOS message is sent by the service provider to indicate the updated values.

## -parameters

### -param dwRequestID

Identifier for reporting asynchronous function results.

### -param hdCall

The service provider's handle to the call.

### -param lpSendingFlowspec

Pointer to memory containing a WinSock2 <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory in the application process, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.

### -param dwSendingFlowspecSize

The total size in bytes of the <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> and accompanying provider-specific data, equivalent to what would have been stored in SendingFlowspec.len in a WinSock2 <a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure.

### -param lpReceivingFlowspec

Pointer to memory containing a WinSock2 <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory in the application process, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.

### -param dwReceivingFlowspecSize

The total size in bytes of the <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> and accompanying provider-specific data, equivalent to what would have been stored in ReceivingFlowspec.len in a WinSock2 <a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a> structure.

## -returns

Returns <b>dwRequestID</b> if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALCALLSTATE, LINEERR_INVALRATE, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_RATEUNAVAIL, LINEERR_RESOURCEUNAVAIL.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>
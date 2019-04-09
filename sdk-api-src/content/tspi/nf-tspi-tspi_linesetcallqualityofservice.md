---
UID: NF:tspi.TSPI_lineSetCallQualityOfService
title: TSPI_lineSetCallQualityOfService function (tspi.h)
author: windows-sdk-content
description: The TSPI_lineSetCallQualityOfService function service provider attempts to renegotiate the QOS on the call with the switch If the desired QOS is not available, then the function fails, but the call continues with the previous QOS.
old-location: tspi\tspi_linesetcallqualityofservice.htm
tech.root: Tapi
ms.assetid: ebef3ee3-94e3-4aef-831d-5ce031882b5c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetCallQualityOfService, TSPI_lineSetCallQualityOfService function [TAPI 2.2], _tspi_tspi_linesetcallqualityofservice, tspi.tspi_linesetcallqualityofservice, tspi/TSPI_lineSetCallQualityOfService
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
 - TSPI_lineSetCallQualityOfService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineSetCallQualityOfService function


## -description


The 
<b>TSPI_lineSetCallQualityOfService</b> function service provider attempts to renegotiate the QOS on the call with the switch If the desired QOS is not available, then the function fails, but the call continues with the previous QOS. If the function succeeds, the new QOS information is stored in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>; a LINECALLINFOSTATE_QOS message is sent by the service provider to indicate the updated values.


## -parameters




### -param dwRequestID

Identifier for reporting asynchronous function results.


### -param hdCall

The service provider's handle to the call.


### -param lpSendingFlowspec

Pointer to memory containing a WinSock2 <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory in the application process, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.


### -param dwSendingFlowspecSize

The total size in bytes of the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> and accompanying provider-specific data, equivalent to what would have been stored in SendingFlowspec.len in a WinSock2 <a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure.


### -param lpReceivingFlowspec

Pointer to memory containing a WinSock2 <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure followed by provider-specific data. The provider-specific portion following the <b>FLOWSPEC</b> structure must not contain pointers to other blocks of memory in the application process, because TAPI does not know how to marshal the data pointed to by the private pointer(s) and convey it through interprocess communication to the service provider.


### -param dwReceivingFlowspecSize

The total size in bytes of the <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> and accompanying provider-specific data, equivalent to what would have been stored in ReceivingFlowspec.len in a WinSock2 <a href="https://msdn.microsoft.com/859faa13-bd66-46ee-8452-6ff5d53d66c9">QOS</a> structure.


## -returns



Returns <b>dwRequestID</b> if the asynchronous operation starts; otherwise, the function returns one of these negative error values:

LINEERR_INVALCALLSTATE, LINEERR_INVALRATE, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_RATEUNAVAIL, LINEERR_RESOURCEUNAVAIL.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>
 

 


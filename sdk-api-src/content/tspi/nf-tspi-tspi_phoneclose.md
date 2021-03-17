---
UID: NF:tspi.TSPI_phoneClose
title: TSPI_phoneClose function (tspi.h)
description: The TSPI_phoneClose function closes the specified open phone device after completing or aborting all outstanding asynchronous operations on the device.
helpviewer_keywords: ["TSPI_phoneClose","TSPI_phoneClose function [TAPI 2.2]","_tspi_tspi_phoneclose","tspi.tspi_phoneclose","tspi/TSPI_phoneClose"]
old-location: tspi\tspi_phoneclose.htm
tech.root: tapi3
ms.assetid: 1db4c460-8afa-4420-9c51-ba276693656e
ms.date: 12/05/2018
ms.keywords: TSPI_phoneClose, TSPI_phoneClose function [TAPI 2.2], _tspi_tspi_phoneclose, tspi.tspi_phoneclose, tspi/TSPI_phoneClose
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
 - TSPI_phoneClose
 - tspi/TSPI_phoneClose
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
 - TSPI_phoneClose
---

# TSPI_phoneClose function


## -description

The 
<b>TSPI_phoneClose</b> function closes the specified open phone device after completing or aborting all outstanding asynchronous operations on the device.

## -parameters

### -param hdPhone

The service provider's opaque handle to the phone to be closed. After the phone is successfully closed, this handle is no longer valid.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INVALPHONEHANDLE, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_RESOURCEUNAVAIL.

## -remarks

The service provider must report completion for every asynchronous operation. If this procedure is called for a phone on which there are outstanding asynchronous operations, the operations should be reported complete with an appropriate result or error code before this procedure returns. Generally, TAPI waits for these to complete in an orderly fashion. However, the service provider should be prepared to handle an early call to 
<b>TSPI_phoneClose</b> in "abort" or "emergency shutdown" situations.

After this procedure returns the service provider must report no further events on the phone. The service provider's opaque handle for the phone becomes invalid.

The service provider must relinquish nonsharable resources it reserves while the phone is open. For example, closing a phone accessed through a comm port and modem should result in closing the comm port, making it available for use by other applications.

This function should always succeed except in extraordinary circumstances. Most callers will probably ignore the return code because they will be unable to compensate for any error that occurs. The specified return values are more advisory for development diagnostic purposes than anything else.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms725255(v=vs.85)">PHONE_CLOSE</a>
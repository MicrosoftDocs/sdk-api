---
UID: NF:msajtransport.AllJoynSendToBus
title: AllJoynSendToBus function (msajtransport.h)
description: Sends data to the bus via named pipe. The caller of this API is responsible to check if the bytesTransferred is less than the requested bytes and call this API again to resend the rest of the data.
helpviewer_keywords: ["AllJoynSendToBus","AllJoynSendToBus function [AllJoyn API]","alljoyn.alljoynsendtobus","msajtransport/AllJoynSendToBus"]
old-location: alljoyn\alljoynsendtobus.htm
tech.root: AllJoyn
ms.assetid: 8D941DB8-AA73-472B-92E2-85EA72BD9A40
ms.date: 12/05/2018
ms.keywords: AllJoynSendToBus, AllJoynSendToBus function [AllJoyn API], alljoyn.alljoynsendtobus, msajtransport/AllJoynSendToBus
req.header: msajtransport.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: MSAJApi.lib
req.dll: MSAJApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AllJoynSendToBus
 - msajtransport/AllJoynSendToBus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - MSAJApi.dll
api_name:
 - AllJoynSendToBus
---

# AllJoynSendToBus function


## -description

Sends data to the bus via named pipe. The caller of this API is responsible to check if the <i>bytesTransferred</i> is less than the   
requested bytes and call this API again to resend the rest of the data.

When the named pipe <i>outBufferSize</i> is less than the <i>bytesToWrite</i>, writing to named pipe is returning TRUE and <i>bytesTransferred == 0</i>, rather than returning TRUE
	   and transferring as much as possible.

## -parameters

### -param connectedBusHandle [in]

Pipe handle.

### -param buffer [in]

Input data buffer.

### -param bytesToWrite [in]

Number of bytes to send.

### -param bytesTransferred [out, optional]

Number of bytes written.

### -param reserved [in, out]

May be used in a future version as OVERLAPPED address. Currently must be NULL.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
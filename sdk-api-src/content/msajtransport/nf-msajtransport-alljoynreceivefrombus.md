---
UID: NF:msajtransport.AllJoynReceiveFromBus
title: AllJoynReceiveFromBus function (msajtransport.h)
description: Receives data from the bus via named pipe.
helpviewer_keywords: ["AllJoynReceiveFromBus","AllJoynReceiveFromBus function [AllJoyn API]","alljoyn.alljoynreceivefrombus","msajtransport/AllJoynReceiveFromBus"]
old-location: alljoyn\alljoynreceivefrombus.htm
tech.root: AllJoyn
ms.assetid: 5E11BCDC-319C-4C53-914E-73B2FEC4747E
ms.date: 12/05/2018
ms.keywords: AllJoynReceiveFromBus, AllJoynReceiveFromBus function [AllJoyn API], alljoyn.alljoynreceivefrombus, msajtransport/AllJoynReceiveFromBus
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
 - AllJoynReceiveFromBus
 - msajtransport/AllJoynReceiveFromBus
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
 - AllJoynReceiveFromBus
---

# AllJoynReceiveFromBus function


## -description

Receives data from the bus via named pipe.

## -parameters

### -param connectedBusHandle [in]

Pipe handle.

### -param buffer [out]

Output data buffer.

### -param bytesToRead [in]

Number of bytes to receive.

### -param bytesTransferred [out, optional]

Number of bytes read.

### -param reserved [in, out]

May be used in a future version as OVERLAPPED address. Currently must be NULL.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
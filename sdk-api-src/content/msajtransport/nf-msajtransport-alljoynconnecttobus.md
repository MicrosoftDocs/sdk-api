---
UID: NF:msajtransport.AllJoynConnectToBus
title: AllJoynConnectToBus function (msajtransport.h)
description: Opens the AllJoyn Router Node Service named pipe, and sets it to PIPE_NOWAIT.
helpviewer_keywords: ["AllJoynConnectToBus","AllJoynConnectToBus function [AllJoyn API]","alljoyn.alljoynconnecttobus","msajtransport/AllJoynConnectToBus"]
old-location: alljoyn\alljoynconnecttobus.htm
tech.root: AllJoyn
ms.assetid: B1929CE6-3707-4660-92CA-E267B1E5B9CC
ms.date: 12/05/2018
ms.keywords: AllJoynConnectToBus, AllJoynConnectToBus function [AllJoyn API], alljoyn.alljoynconnecttobus, msajtransport/AllJoynConnectToBus
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
 - AllJoynConnectToBus
 - msajtransport/AllJoynConnectToBus
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
 - AllJoynConnectToBus
---

# AllJoynConnectToBus function


## -description

Opens the AllJoyn Router Node Service named pipe, and sets it to <b>PIPE_NOWAIT</b>.

## -parameters

### -param connectionSpec [in, optional]

Optional parameter to pass connection spec for future use.

## -returns

The client side handle.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INVALID_HANDLE_VALUE</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.  Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for more information.  The app can retry the <a href="/previous-versions/windows/desktop/api/msajtransport/nf-msajtransport-alljoynconnecttobus">ConnectToBus</a> in case of GetLastError() == <b>ERROR_PIPE_BUSY</b>.  In AllJoyn, we allow multiple instances of server, so <b>ERROR_PIPE_BUSY</b> is not expected to occur in a normal use case.

</td>
</tr>
</table>
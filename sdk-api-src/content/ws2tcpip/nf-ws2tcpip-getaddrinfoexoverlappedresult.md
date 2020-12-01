---
UID: NF:ws2tcpip.GetAddrInfoExOverlappedResult
title: GetAddrInfoExOverlappedResult function (ws2tcpip.h)
description: Gets the return code for an OVERLAPPED structure used by an asynchronous operation for the GetAddrInfoEx function.
helpviewer_keywords: ["GetAddrInfoExOverlappedResult","GetAddrInfoExOverlappedResult function [Winsock]","winsock.getaddrinfoexoverlappedresult","ws2tcpip/GetAddrInfoExOverlappedResult"]
old-location: winsock\getaddrinfoexoverlappedresult.htm
tech.root: WinSock
ms.assetid: BBA6E407-561C-4B3C-9218-0047477E82DE
ms.date: 12/05/2018
ms.keywords: GetAddrInfoExOverlappedResult, GetAddrInfoExOverlappedResult function [Winsock], winsock.getaddrinfoexoverlappedresult, ws2tcpip/GetAddrInfoExOverlappedResult
req.header: ws2tcpip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1, Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ws2_32.lib
req.dll: Ws2_32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAddrInfoExOverlappedResult
 - ws2tcpip/GetAddrInfoExOverlappedResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ws2_32.dll
api_name:
 - GetAddrInfoExOverlappedResult
---

# GetAddrInfoExOverlappedResult function


## -description

The 
<b>GetAddrInfoExOverlappedResult</b> function gets the return code for an <b>OVERLAPPED</b> structure used by an asynchronous operation for the  <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function.

## -parameters

### -param lpOverlapped

A pointer to an <b>OVERLAPPED</b> structure for the asynchronous operation.

## -returns

On success,  the <b>GetAddrInfoExOverlappedResult</b> function returns <b>NO_ERROR</b> (0). When the
    underlying operation hasn't yet completed, the <b>GetAddrInfoExOverlappedResult</b> function  returns <b>WSAEINPROGRESS</b>. On failure, the <b>GetAddrInfoExOverlappedResult</b> function  returns <b>WSAEINVAL</b>.

## -remarks

The 
<b>GetAddrInfoExOverlappedResult</b> function is used with the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> function for asynchronous operations.

If the <b>GetAddrInfoExOverlappedResult</b> function returns <b>WSAEINVAL</b>, the only way to distinguish whether <b>GetAddrInfoExOverlappedResult</b> function or the asynchronous operation returned  the
    error is to check that the <i>lpOverlapped</i> parameter was not NULL. If the <i>lpOverlapped</i> parameter was NULL, then the <b>GetAddrInfoExOverlappedResult</b> function was passed a NULL pointer and failed. 

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.

## -see-also

<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>
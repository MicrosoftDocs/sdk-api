---
UID: NF:sensapi.IsDestinationReachableW
title: IsDestinationReachableW function (sensapi.h)
description: The IsDestinationReachable function determines whether or not a specified destination can be reached, and provides Quality of Connection (QOC) information for a destination. (Unicode)
helpviewer_keywords: ["IsDestinationReachable", "IsDestinationReachable function [SENS]", "IsDestinationReachableW", "_zaw_isdestinationreachable", "sens.isdestinationreachable", "sensapi/IsDestinationReachable", "sensapi/IsDestinationReachableW", "syncmgr.isdestinationreachable"]
old-location: sens\isdestinationreachable.htm
tech.root: Sens
ms.assetid: 377af331-8494-4a3d-b822-78c2b568239c
ms.date: 12/05/2018
ms.keywords: IsDestinationReachable, IsDestinationReachable function [SENS], IsDestinationReachableA, IsDestinationReachableW, _zaw_isdestinationreachable, sens.isdestinationreachable, sensapi/IsDestinationReachable, sensapi/IsDestinationReachableA, sensapi/IsDestinationReachableW, syncmgr.isdestinationreachable
req.header: sensapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsDestinationReachableW (Unicode) and IsDestinationReachableA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sensapi.lib
req.dll: Sensapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsDestinationReachableW
 - sensapi/IsDestinationReachableW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sensapi.dll
api_name:
 - IsDestinationReachable
 - IsDestinationReachableA
 - IsDestinationReachableW
---

# IsDestinationReachableW function


## -description

The 
<b>IsDestinationReachable</b> function determines whether or not  a specified destination can be reached, and provides Quality of Connection (QOC) information for a destination.

<b>Windows Vista and later, Windows Server 2008 and later:  </b>This function is not supported and always returns <b>ERROR_CALL_NOT_IMPLEMENTED</b>.

## -parameters

### -param lpszDestination [in]

A pointer to a <b>null</b>-terminated string that specifies a destination. The destination can be an IP address, UNC name, or URL.

### -param lpQOCInfo [in, out]

A pointer to the 
<a href="/windows/desktop/api/sensapi/ns-sensapi-qocinfo">QOCINFO</a> structure that receives the Quality of Connection (QOC) information. You can supply a <b>NULL</b> pointer if you do not want to receive the QOC information.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
A destination can be reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
A destination cannot be reached. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CALL_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not available on Windows Vista.

</td>
</tr>
</table>

## -remarks

Client applications use this function to determine the QOC information before proceeding with network operations. For standalone computers that are directly connected to a network through a network card or remote access server (RAS), this function generates minimal network traffic with RPC calls to the nearest router. For computers that are part of a network where a destination can be reached by using RAS or a network gateway, this function pings a destination to generate accurate QOC information.

This function is only available for TCP/IP connections. A caller supplies the buffer for the 
<a href="/windows/desktop/api/sensapi/ns-sensapi-qocinfo">QOCINFO</a> structure, and must release the memory when it is not needed.

Starting with applications designed for Windows Vista and Windows Server 2008, developers should consider using the <a href="/windows/desktop/NLA/portal">Network List Manager</a> instead of this function.







> [!NOTE]
> The sensapi.h header defines IsDestinationReachable as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Sens/about-system-event-notification-service">About System Event Notification Service</a>



<a href="/windows/desktop/api/sensapi/nf-sensapi-isnetworkalive">IsNetworkAlive</a>



<a href="/windows/desktop/api/sensapi/ns-sensapi-qocinfo">QOCINFO</a>

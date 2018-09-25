---
UID: NF:tapi.lineGetAgentCapsW
title: lineGetAgentCapsW function
author: windows-sdk-content
description: The lineGetAgentCaps function obtains the agent-related capabilities supported on the specified line device. If a specific agent is named, the capabilities include a listing of ACD groups into which the agent is permitted to log in.
old-location: tapi2\linegetagentcaps.htm
tech.root: tapi
ms.assetid: 04bb6c00-2654-4707-ab11-2490ab5d9ab0
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "_tapi2_linegetagentcaps, lineGetAgentCaps, lineGetAgentCaps function [TAPI 2.2], lineGetAgentCapsA, lineGetAgentCapsW, tapi/lineGetAgentCaps, tapi/lineGetAgentCapsA, tapi/lineGetAgentCapsW, tapi2.linegetagentcaps"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineGetAgentCapsW (Unicode) and lineGetAgentCapsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineGetAgentCaps
 - lineGetAgentCapsA
 - lineGetAgentCapsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineGetAgentCapsW function


## -description


The 
<b>lineGetAgentCaps</b> function obtains the agent-related capabilities supported on the specified line device. If a specific agent is named, the capabilities include a listing of ACD groups into which the agent is permitted to log in.


## -parameters




### -param hLineApp

Handle to the application's registration with TAPI.


### -param dwDeviceID

Line device containing the address to be queried.


### -param dwAddressID

Address on the given line device whose capabilities are to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param dwAppAPIVersion

Highest API version supported by the application. This should not be the value negotiated using 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a> on the device being queried.


### -param lpAgentCaps

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/e4c5ece8-7b29-4154-9b38-f2b17049446f">LINEAGENTCAPS</a>. Upon successful completion of the request, this structure is filled with agent capabilities information. Prior to calling 
<b>lineGetAgentCaps</b>, the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, this function returns one of these negative error values:

LINEERR_BADDEVICEID, LINEERR_INCOMPATIBLEAPIVERSION, LINEERR_INVALADDRESSID, LINEERR_INVALAPPHANDLE, LINEERR_INVALPOINTER, LINEERR_NODEVICE, LINEERR_NODRIVER, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_STRUCTURETOOSMALL, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/e4c5ece8-7b29-4154-9b38-f2b17049446f">LINEAGENTCAPS</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>
 

 


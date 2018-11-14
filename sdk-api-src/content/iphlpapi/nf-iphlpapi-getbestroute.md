---
UID: NF:iphlpapi.GetBestRoute
title: GetBestRoute function
author: windows-sdk-content
description: The GetBestRoute function retrieves the best route to the specified destination IP address.
old-location: iphlp\getbestroute.htm
tech.root: IpHlp
ms.assetid: 5e507d14-f603-467d-9c37-bb048658d0b1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetBestRoute, GetBestRoute function [IP Helper], _iphlp_getbestroute, iphlp.getbestroute, iphlpapi/GetBestRoute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetBestRoute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetBestRoute
: 
---

# GetBestRoute function


## -description


The 
<b>GetBestRoute</b> function retrieves the best route to the specified destination IP address.


## -parameters




### -param dwDestAddr [in]

Destination IP address for which to obtain the best route.


### -param dwSourceAddr [in]

Source IP address. This IP address corresponds to an interface on the local computer. If multiple best routes to the destination address exist, the function selects the route that uses this interface. 




This parameter is optional. The caller may specify zero for this parameter.


### -param pBestRoute [out]

Pointer to a 
<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structure containing the best route for the IP address specified by <i>dwDestAddr</i>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.




## -see-also




<a href="https://msdn.microsoft.com/9171cdf7-4057-4a8d-a34c-1b7b1f94bcb1">GetBestInterface</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a>
 

 


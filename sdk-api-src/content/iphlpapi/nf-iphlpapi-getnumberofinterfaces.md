---
UID: NF:iphlpapi.GetNumberOfInterfaces
title: GetNumberOfInterfaces function (iphlpapi.h)
description: The GetNumberOfInterfaces functions retrieves the number of interfaces on the local computer.
helpviewer_keywords: ["GetNumberOfInterfaces","GetNumberOfInterfaces function [IP Helper]","_iphlp_getnumberofinterfaces","iphlp.getnumberofinterfaces","iphlpapi/GetNumberOfInterfaces"]
old-location: iphlp\getnumberofinterfaces.htm
tech.root: IpHlp
ms.assetid: 655d63eb-455a-4a5e-97e2-7b7588eee4d9
ms.date: 12/05/2018
ms.keywords: GetNumberOfInterfaces, GetNumberOfInterfaces function [IP Helper], _iphlp_getnumberofinterfaces, iphlp.getnumberofinterfaces, iphlpapi/GetNumberOfInterfaces
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNumberOfInterfaces
 - iphlpapi/GetNumberOfInterfaces
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetNumberOfInterfaces
---

# GetNumberOfInterfaces function


## -description

The 
<b>GetNumberOfInterfaces</b> functions retrieves the number of interfaces on the local computer.

## -parameters

### -param pdwNumIf [out]

Pointer to a <b>DWORD</b> variable that receives the number of interfaces on the local computer.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

## -remarks

The 
<b>GetNumberOfInterfaces</b> function returns the number of interfaces on the local computer, including the loopback interface. This number is one more than the number of adapters returned by the 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a> and 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getinterfaceinfo">GetInterfaceInfo</a> functions because these functions do not return information about the loopback interface.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getifentry">GetIfEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getinterfaceinfo">GetInterfaceInfo</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>
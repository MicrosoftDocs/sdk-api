---
UID: NF:iphlpapi.GetUniDirectionalAdapterInfo
title: GetUniDirectionalAdapterInfo function (iphlpapi.h)
description: The GetUniDirectionalAdapterInfo function retrieves information about the unidirectional adapters installed on the local computer. A unidirectional adapter is an adapter that can receive datagrams, but not transmit them.
helpviewer_keywords: ["GetUniDirectionalAdapterInfo","GetUniDirectionalAdapterInfo function [IP Helper]","_iphlp_getunidirectionaladapterinfo","iphlp.getunidirectionaladapterinfo","iphlpapi/GetUniDirectionalAdapterInfo"]
old-location: iphlp\getunidirectionaladapterinfo.htm
tech.root: IpHlp
ms.assetid: 32aa3a8e-ae74-4da9-bc8d-b28e270d9702
ms.date: 12/05/2018
ms.keywords: GetUniDirectionalAdapterInfo, GetUniDirectionalAdapterInfo function [IP Helper], _iphlp_getunidirectionaladapterinfo, iphlp.getunidirectionaladapterinfo, iphlpapi/GetUniDirectionalAdapterInfo
req.header: iphlpapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetUniDirectionalAdapterInfo
 - iphlpapi/GetUniDirectionalAdapterInfo
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
 - GetUniDirectionalAdapterInfo
---

# GetUniDirectionalAdapterInfo function


## -description

The 
<b>GetUniDirectionalAdapterInfo</b> function retrieves information about the unidirectional adapters installed on the local computer. A unidirectional adapter is an adapter that can receive datagrams, but not transmit them.

## -parameters

### -param pIPIfInfo [out]

Pointer to an 
<a href="/windows/win32/api/ipexport/ns-ipexport-ip_unidirectional_adapter_address">IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</a> structure that receives information about the unidirectional adapters installed on the local computer.

### -param dwOutBufLen [out]

Pointer to a <b>ULONG</b> variable that receives the size of the structure pointed to by the <i>pIPIfInfo</i> parameter.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/win32/api/ipexport/ns-ipexport-ip_unidirectional_adapter_address">IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</a>
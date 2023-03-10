---
UID: NF:netioapi.GetDefaultCompartmentId
title: GetDefaultCompartmentId function (netioapi.h)
description: The GetDefaultCompartmentId function retrieves the default network routing compartment identifier for the local computer.
helpviewer_keywords: ["GetDefaultCompartmentId","GetDefaultCompartmentId function [IP Helper]","iphlp.getdefaultcompartmentid","netioapi/GetDefaultCompartmentId"]
old-location: iphlp\getdefaultcompartmentid.htm
tech.root: IpHlp
ms.assetid: 6747534F-7121-4783-BC19-D564C7014815
ms.date: 12/05/2018
ms.keywords: GetDefaultCompartmentId, GetDefaultCompartmentId function [IP Helper], iphlp.getdefaultcompartmentid, netioapi/GetDefaultCompartmentId
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - GetDefaultCompartmentId
 - netioapi/GetDefaultCompartmentId
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
 - GetDefaultCompartmentId
---

# GetDefaultCompartmentId function


## -description

The 
<b>GetDefaultCompartmentId</b> function retrieves the default network routing compartment identifier for the local computer.



## -returns

If the function succeeds, the return value is the default Compartment ID.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NET_IF_COMPARTMENT_ID_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
The function failed to obtain a Compartment ID.

</td>
</tr>
</table>


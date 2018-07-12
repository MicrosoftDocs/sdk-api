---
UID: NF:netioapi.GetDefaultCompartmentId
title: GetDefaultCompartmentId function
author: windows-sdk-content
description: The GetDefaultCompartmentId function retrieves the default network routing compartment identifier for the local computer.
old-location: iphlp\getdefaultcompartmentid.htm
old-project: iphlp
ms.assetid: 6747534F-7121-4783-BC19-D564C7014815
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetDefaultCompartmentId, GetDefaultCompartmentId function [IP Helper], iphlp.getdefaultcompartmentid, netioapi/GetDefaultCompartmentId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetDefaultCompartmentId
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetDefaultCompartmentId function


## -description


The 
<b>GetDefaultCompartmentId</b> function retrieves the default network routing compartment identifier for the local computer.
		


## -parameters






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
 




---
UID: NS:routprot.IP_LOCAL_BINDING
title: IP_LOCAL_BINDING
author: windows-sdk-content
description: The IP_LOCAL_BINDING structure contains IP address information for an adapter.
old-location: rras\ip_local_binding.htm
tech.root: rras
ms.assetid: 121cc415-35eb-4c9b-a02d-c23be468d6bc
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PIP_LOCAL_BINDING, IP_LOCAL_BINDING, IP_LOCAL_BINDING structure [RAS], PIP_LOCAL_BINDING, PIP_LOCAL_BINDING structure pointer [RAS], _mpr_ip_local_binding, routprot/IP_LOCAL_BINDING, routprot/PIP_LOCAL_BINDING, rras.ip_local_binding"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: routprot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Routprot.h
api_name:
 - IP_LOCAL_BINDING
product: Windows
targetos: Windows
req.typenames: IP_LOCAL_BINDING, *PIP_LOCAL_BINDING
req.redist: 
---

# IP_LOCAL_BINDING structure


## -description


The 
<b>IP_LOCAL_BINDING</b> structure contains IP address information for an adapter.


## -struct-fields




### -field Address

Specifies an IP address for the adapter.


### -field Mask

Specifies the subnet mask for the IP address.


## -remarks



Since an adapter can have more than one IP address, the 
<a href="https://msdn.microsoft.com/3eb864e7-2de6-44c2-af3e-fee547de6081">IP_ADAPTER_BINDING_INFO</a> structure maintains an array of 
<b>IP_LOCAL_BINDING</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/3eb864e7-2de6-44c2-af3e-fee547de6081">IP_ADAPTER_BINDING_INFO</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 


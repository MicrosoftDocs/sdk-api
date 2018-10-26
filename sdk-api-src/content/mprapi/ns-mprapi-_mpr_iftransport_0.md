---
UID: NS:mprapi._MPR_IFTRANSPORT_0
title: "_MPR_IFTRANSPORT_0"
author: windows-sdk-content
description: The MPR_IFTRANSPORT_0 structure contains information for a particular interface transport.
old-location: rras\mpr_iftransport_0.htm
tech.root: rras
ms.assetid: 4ee360be-fe5f-477e-901f-92d083f68451
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PMPR_IFTRANSPORT_0, MPR_IFTRANSPORT_0, MPR_IFTRANSPORT_0 structure [RAS], PMPR_IFTRANSPORT_0, PMPR_IFTRANSPORT_0 structure pointer [RAS], _MPR_IFTRANSPORT_0, _mpr_mpr_iftransport_0, mprapi/MPR_IFTRANSPORT_0, mprapi/PMPR_IFTRANSPORT_0, rras.mpr_iftransport_0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
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
 - Mprapi.h
api_name:
 - MPR_IFTRANSPORT_0
product: Windows
targetos: Windows
req.typenames: MPR_IFTRANSPORT_0, *PMPR_IFTRANSPORT_0
req.redist: 
---

# _MPR_IFTRANSPORT_0 structure


## -description


The 
<b>MPR_IFTRANSPORT_0</b> structure contains information for a particular interface transport.


## -struct-fields




### -field dwTransportId

Identifies the transport.


### -field hIfTransport

Handle to the interface transport.


### -field wszIfTransportName

Specifies a Unicode string that contains the name of the interface transport.


## -see-also




<a href="https://msdn.microsoft.com/f5515a39-377d-4767-b508-2306832d81f7">MPR_TRANSPORT_0</a>



<a href="https://msdn.microsoft.com/ae395eb8-8019-432c-bf96-b602c8e34f12">MprConfigInterfaceTransportEnum</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 


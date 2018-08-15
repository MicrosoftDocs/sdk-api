---
UID: NS:mprapi._MPR_TRANSPORT_0
title: "_MPR_TRANSPORT_0"
author: windows-sdk-content
description: The MPR_TRANSPORT_0 structure contains information for a particular transport.
old-location: rras\mpr_transport_0.htm
old-project: rras
ms.assetid: f5515a39-377d-4767-b508-2306832d81f7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMPR_TRANSPORT_0, MPR_TRANSPORT_0, MPR_TRANSPORT_0 structure [RAS], PMPR_TRANSPORT_0, PMPR_TRANSPORT_0 structure pointer [RAS], _MPR_TRANSPORT_0, _mpr_mpr_transport_0, mprapi/MPR_TRANSPORT_0, mprapi/PMPR_TRANSPORT_0, rras.mpr_transport_0"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mprapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MPR_TRANSPORT_0, *PMPR_TRANSPORT_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_TRANSPORT_0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MPR_TRANSPORT_0 structure


## -description


The 
<b>MPR_TRANSPORT_0</b> structure contains information for a particular transport.


## -struct-fields




### -field dwTransportId

A <b>DWORD</b> value that identifies the transport protocol type. Supported transport protocol types are listed on <a href="https://msdn.microsoft.com/7720c34f-0558-49de-8f82-13a67e2c8c69">Transport Identifiers</a>.


### -field hTransport

Handle to the transport.


### -field wszTransportName

A Unicode string that contains the name of the transport.


## -see-also




<a href="https://msdn.microsoft.com/4ee360be-fe5f-477e-901f-92d083f68451">MPR_IFTRANSPORT_0</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 


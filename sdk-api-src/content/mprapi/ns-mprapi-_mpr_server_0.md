---
UID: NS:mprapi._MPR_SERVER_0
title: "_MPR_SERVER_0"
author: windows-sdk-content
description: The MPR_SERVER_0 structure is used to retrieve information about a device.
old-location: rras\mpr_server_0.htm
tech.root: rras
ms.assetid: cffda25b-28f8-4d76-987c-eadcea9c032b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PMPR_SERVER_0, MPR_SERVER_0, MPR_SERVER_0 structure [RAS], PMPR_SERVER_0, PMPR_SERVER_0 structure pointer [RAS], _MPR_SERVER_0, _mpr_mpr_server_0, mprapi/MPR_SERVER_0, mprapi/PMPR_SERVER_0, rras.mpr_server_0"
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
 - MPR_SERVER_0
product: Windows
targetos: Windows
req.typenames: MPR_SERVER_0, *PMPR_SERVER_0
req.redist: 
---

# _MPR_SERVER_0 structure


## -description


The 
<b>MPR_SERVER_0</b> structure is used to retrieve information about a device.


## -struct-fields




### -field fLanOnlyMode

A <b>BOOL</b> that specifies whether the Demand Dial Manager (DDM) is running on the device. If <b>TRUE</b>, the DDM is not running on the device. Otherwise, it is <b>FALSE</b>.


### -field dwUpTime

Specifies the elapsed time, in seconds, since the device was started.


### -field dwTotalPorts

Specifies the number of ports on the device.


### -field dwPortsInUse

Specifies the number of ports currently in use on the device.


## -see-also




<a href="https://msdn.microsoft.com/ea27a928-055b-4705-8f7c-dd9a221b2573">MPR_SERVER_1</a>



<a href="https://msdn.microsoft.com/9e38651a-541f-4470-a841-4eb94dbe4835">MPR_SERVER_2</a>



<a href="https://msdn.microsoft.com/d15dfb60-1239-4552-985f-d3c98f2981f4">MprAdminServerGetInfo</a>



<a href="https://msdn.microsoft.com/6d3cd97a-96ef-4ecd-b2fd-2743ba79aa5b">MprConfigServerGetInfo</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>



<a href="https://msdn.microsoft.com/767733eb-1cbd-4b8d-98b7-41d1d0f2c630">Router Management Structures</a>
 

 


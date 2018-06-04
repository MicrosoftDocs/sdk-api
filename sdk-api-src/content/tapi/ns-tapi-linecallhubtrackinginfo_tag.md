---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# linecallhubtrackinginfo_tag structure


## -description


The 
<b>LINECALLHUBTRACKINGINFO</b> structure contains information that reports the type of tracking available to a call hub. This structure is exposed only to applications that negotiate a TAPI version of 2.2 or higher.

The 
<a href="https://msdn.microsoft.com/ec2d5d46-1c83-47a0-9c10-684959630a16">TSPI_lineSetCallHubTracking</a> function and the 
<a href="https://msdn.microsoft.com/c8fd8070-7393-4a59-9416-63acdd94f4ff">TSPI_lineGetCallHubTracking</a> function use the 
<b>LINECALLHUBTRACKINGINFO</b> structure.


## -struct-fields




### -field dwTotalSize

Total size, in bytes.


### -field dwNeededSize

Size needed, in bytes.


### -field dwUsedSize

Size used, in bytes.


### -field dwAvailableTracking

Available tracking, as represented by a 
<a href="https://msdn.microsoft.com/ad3c8d2e-f074-4db0-bb72-fb2181cbf687">LINECALLHUBTRACKING</a>.constant.


### -field dwCurrentTracking

Current tracking, as represented by a <a href="https://msdn.microsoft.com/ad3c8d2e-f074-4db0-bb72-fb2181cbf687">LINECALLHUBTRACKING</a> constant.


## -see-also




<a href="https://msdn.microsoft.com/ad3c8d2e-f074-4db0-bb72-fb2181cbf687">LINECALLHUBTRACKING</a>



<a href="https://msdn.microsoft.com/c8fd8070-7393-4a59-9416-63acdd94f4ff">TSPI_lineGetCallHubTracking</a>



<a href="https://msdn.microsoft.com/ec2d5d46-1c83-47a0-9c10-684959630a16">TSPI_lineSetCallHubTracking</a>
 

 


---
UID: NS:tapi.linecallhubtrackinginfo_tag
title: linecallhubtrackinginfo_tag
author: windows-sdk-content
description: The LINECALLHUBTRACKINGINFO structure contains information that reports the type of tracking available to a call hub. This structure is exposed only to applications that negotiate a TAPI version of 2.2 or higher.
old-location: tapi2\linecallhubtrackinginfo_str.htm
tech.root: tapi
ms.assetid: 1f4eaf7d-fc80-4131-af5a-30c6869c74ef
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*LPLINECALLHUBTRACKINGINFO, LINECALLHUBTRACKINGINFO, LINECALLHUBTRACKINGINFO structure [TAPI 2.2], LPLINECALLHUBTRACKINGINFO, LPLINECALLHUBTRACKINGINFO structure pointer [TAPI 2.2], _tapi2_linecallhubtrackinginfo_str, linecallhubtrackinginfo_tag, tapi/LINECALLHUBTRACKINGINFO, tapi/LPLINECALLHUBTRACKINGINFO, tapi2.linecallhubtrackinginfo_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINECALLHUBTRACKINGINFO
product: Windows
targetos: Windows
req.typenames: LINECALLHUBTRACKINGINFO, *LPLINECALLHUBTRACKINGINFO
req.redist: 
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
 

 


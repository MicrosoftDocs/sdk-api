---
UID: NS:tapi.linequeuelist_tag
title: linequeuelist_tag
author: windows-sdk-content
description: The LINEQUEUELIST structure describes a list of queues. This structure can contain an array of LINEQUEUEENTRY structures. The lineGetQueueList function returns the LINEQUEUELIST structure. LINEQUEUELIST requires TAPI 3.0 version negotiation.
old-location: tapi2\linequeuelist.htm
tech.root: tapi
ms.assetid: 86645d7c-f683-48e7-8342-3e9d5961913a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPLINEQUEUELIST, LINEQUEUELIST, LINEQUEUELIST structure [TAPI 2.2], LPLINEQUEUELIST, LPLINEQUEUELIST structure pointer [TAPI 2.2], _tapi2_linequeuelist, linequeuelist_tag, tapi/LINEQUEUELIST, tapi/LPLINEQUEUELIST, tapi2.linequeuelist"
ms.prod: windows
ms.technology: windows-sdk
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
 - LINEQUEUELIST
product: Windows
targetos: Windows
req.typenames: LINEQUEUELIST, *LPLINEQUEUELIST
req.redist: 
---

# linequeuelist_tag structure


## -description


The 
<b>LINEQUEUELIST</b> structure describes a list of queues. This structure can contain an array of 
<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a> structures. The 
<a href="https://msdn.microsoft.com/3921ab24-c9c8-4068-a885-e55759f04076">lineGetQueueList</a> function returns the 
<b>LINEQUEUELIST</b> structure. 
<b>LINEQUEUELIST</b> requires TAPI 3.0 version negotiation.


## -struct-fields




### -field dwTotalSize

Total size allocated to this structure, in bytes.


### -field dwNeededSize

Size needed to hold all the information requested, in bytes.


### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.


### -field dwNumEntries

Number of 
<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a> structures that appear in the list array. The value is zero if no queue is available.


### -field dwListSize

Size of the agent information array, in bytes.


### -field dwListOffset

Offset from the beginning of the structure to an array of 
<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a> structure that specify information about agents. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(LINEQUEUEENTRY). The size of the field is specified by <b>dwListSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/b05eb100-2a43-421f-826b-c37d05e4ef14">LINEQUEUEENTRY</a>



<a href="https://msdn.microsoft.com/3921ab24-c9c8-4068-a885-e55759f04076">lineGetQueueList</a>
 

 


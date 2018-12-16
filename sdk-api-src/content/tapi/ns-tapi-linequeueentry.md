---
UID: NS:tapi.linequeueentry_tag
title: LINEQUEUEENTRY
author: windows-sdk-content
description: The LINEQUEUEENTRY structure provides the information for a single queue entry. The LINEQUEUELIST structure can contain an array of LINEQUEUEENTRY structures. This structure requires TAPI 3.0 version negotiation.
old-location: tapi2\linequeueentry.htm
tech.root: tapi
ms.assetid: b05eb100-2a43-421f-826b-c37d05e4ef14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPLINEQUEUEENTRY, LINEQUEUEENTRY, LINEQUEUEENTRY structure [TAPI 2.2], LPLINEQUEUEENTRY, LPLINEQUEUEENTRY structure pointer [TAPI 2.2], _tapi2_linequeueentry, tapi/LINEQUEUEENTRY, tapi/LPLINEQUEUEENTRY, tapi2.linequeueentry"
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
 - LINEQUEUEENTRY
product: Windows
targetos: Windows
req.typenames: LINEQUEUEENTRY, *LPLINEQUEUEENTRY
req.redist: 
---

# LINEQUEUEENTRY structure


## -description


The 
<b>LINEQUEUEENTRY</b> structure provides the information for a single queue entry. The 
<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a> structure can contain an array of 
<b>LINEQUEUEENTRY</b> structures. This structure requires TAPI 3.0 version negotiation.


## -struct-fields




### -field dwQueueID

Unique identifier for a queue. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.


### -field dwNameSize

Size of the queue name string including the <b>null</b> terminator, in bytes.


### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the name of the queue. The size of the string is specified by <b>dwNameSize</b>.


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/86645d7c-f683-48e7-8342-3e9d5961913a">LINEQUEUELIST</a>



<a href="https://msdn.microsoft.com/3921ab24-c9c8-4068-a885-e55759f04076">lineGetQueueList</a>
 

 


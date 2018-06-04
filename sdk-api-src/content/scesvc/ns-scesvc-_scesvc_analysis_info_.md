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

# _SCESVC_ANALYSIS_INFO_ structure


## -description


The <b>SCESVC_ANALYSIS_INFO</b> structure contains the analysis information. It contains a 
<a href="https://msdn.microsoft.com/91fa0f25-30e1-4af3-ad22-f16dc4692b0b">SCESVC_ANALYSIS_LINE</a> structure that contains lines of analysis information, and it also contains a counter that indicates the number of lines.

A pointer to this structure is returned by calls to 
<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a> and 
<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a> when analysis information is specified.


## -struct-fields




### -field Count

A <b>DWORD</b> that indicates the number of lines in the array.


### -field Lines

Pointer to an array of 
<a href="https://msdn.microsoft.com/91fa0f25-30e1-4af3-ad22-f16dc4692b0b">SCESVC_ANALYSIS_LINE</a> structures which contain the analysis information.


## -see-also




<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a>



<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a>



<a href="https://msdn.microsoft.com/91fa0f25-30e1-4af3-ad22-f16dc4692b0b">SCESVC_ANALYSIS_LINE</a>



<a href="https://msdn.microsoft.com/697dfecf-46a9-4558-90e2-099fabc60742">SCESVC_INFO_TYPE</a>
 

 


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

# _SCESVC_CONFIGURATION_INFO_ structure


## -description


The <b>SCESVC_CONFIGURATION_INFO</b> structure provides configuration information for a service. This structure is used by the 
<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a> and 
<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a> functions when the configuration information is specified.


## -struct-fields




### -field Count

Indicates the number of lines of data returned in the <b>Lines</b> array.


### -field Lines

Pointer to an array of 
<a href="https://msdn.microsoft.com/25801b20-9a7a-423e-8fa3-86896a8fbae4">SCESVC_CONFIGURATION_LINE</a> structures which contains the configuration data for this service. Each element represents a line in the security template or database.


## -remarks



When analysis information is specified, the 
<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a> and 
<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a> functions use the 
<a href="https://msdn.microsoft.com/4f0273df-435d-4324-b8ce-a774da935059">SCESVC_ANALYSIS_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a>



<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a>



<a href="https://msdn.microsoft.com/25801b20-9a7a-423e-8fa3-86896a8fbae4">SCESVC_CONFIGURATION_LINE</a>



<a href="https://msdn.microsoft.com/697dfecf-46a9-4558-90e2-099fabc60742">SCESVC_INFO_TYPE</a>
 

 


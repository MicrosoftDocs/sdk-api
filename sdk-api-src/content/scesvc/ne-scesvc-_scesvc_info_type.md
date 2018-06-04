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

# _SCESVC_INFO_TYPE enumeration


## -description


The <b>SCESVC_INFO_TYPE</b> enumeration is used by 
<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a> and 
<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a> to indicate the type of information requested from or passed to the security database. It can be one of the following values.


## -enum-fields




### -field SceSvcConfigurationInfo

The data is configuration information.


### -field SceSvcMergedPolicyInfo

The data is merged policy information.


### -field SceSvcAnalysisInfo

The data is analysis information.


### -field SceSvcInternalUse

Reserved. Do not use.


## -see-also




<a href="https://msdn.microsoft.com/a0e4a205-46d4-47c9-97cf-66f6bec34a1b">PFSCE_QUERY_INFO</a>



<a href="https://msdn.microsoft.com/131585a9-b0a9-4686-84ba-237bcdcc4f5f">PFSCE_SET_INFO</a>



<a href="https://msdn.microsoft.com/4f0273df-435d-4324-b8ce-a774da935059">SCESVC_ANALYSIS_INFO</a>



<a href="https://msdn.microsoft.com/a89ab072-7b7c-4ecd-83fa-26e2689778df">SCESVC_CONFIGURATION_INFO</a>
 

 


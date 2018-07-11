---
UID: NS:scesvc._SCESVC_ANALYSIS_INFO_
title: "_SCESVC_ANALYSIS_INFO_"
author: windows-sdk-content
description: Contains the analysis information.
old-location: security\scesvc_analysis_info.htm
old-project: secmgmt
ms.assetid: 4f0273df-435d-4324-b8ce-a774da935059
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: "*PSCESVC_ANALYSIS_INFO, PSCESVC_ANALYSIS_INFO, PSCESVC_ANALYSIS_INFO structure pointer [Security], SCESVC_ANALYSIS_INFO, SCESVC_ANALYSIS_INFO structure [Security], _SCESVC_ANALYSIS_INFO_, _config_scesvc_analysis_info, scesvc/PSCESVC_ANALYSIS_INFO, scesvc/SCESVC_ANALYSIS_INFO, security.scesvc_analysis_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: scesvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SCESVC_ANALYSIS_INFO, *PSCESVC_ANALYSIS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Scesvc.h
api_name:
 - SCESVC_ANALYSIS_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 


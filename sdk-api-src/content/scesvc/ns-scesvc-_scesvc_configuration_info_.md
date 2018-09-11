---
UID: NS:scesvc._SCESVC_CONFIGURATION_INFO_
title: "_SCESVC_CONFIGURATION_INFO_"
author: windows-sdk-content
description: The SCESVC_CONFIGURATION_INFO structure provides configuration information for a service. This structure is used by the PFSCE_QUERY_INFO and PFSCE_SET_INFO functions when the configuration information is specified.
old-location: security\scesvc_configuration_info.htm
tech.root: SecMgmt
ms.assetid: a89ab072-7b7c-4ecd-83fa-26e2689778df
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSCESVC_CONFIGURATION_INFO, PSCESVC_CONFIGURATION_INFO, PSCESVC_CONFIGURATION_INFO structure pointer [Security], SCESVC_CONFIGURATION_INFO, SCESVC_CONFIGURATION_INFO structure [Security], _SCESVC_CONFIGURATION_INFO_, _config_scesvc_configuration_info, scesvc/PSCESVC_CONFIGURATION_INFO, scesvc/SCESVC_CONFIGURATION_INFO, security.scesvc_configuration_info"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Scesvc.h
api_name:
 - SCESVC_CONFIGURATION_INFO
product: Windows
targetos: Windows
req.typenames: SCESVC_CONFIGURATION_INFO, *PSCESVC_CONFIGURATION_INFO
req.redist: 
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
 

 


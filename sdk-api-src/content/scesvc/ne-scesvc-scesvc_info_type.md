---
UID: NE:scesvc._SCESVC_INFO_TYPE
title: SCESVC_INFO_TYPE
author: windows-sdk-content
description: The SCESVC_INFO_TYPE enumeration is used by PFSCE_QUERY_INFO and PFSCE_SET_INFO to indicate the type of information requested from or passed to the security database. It can be one of the following values.
old-location: security\scesvc_info_type.htm
tech.root: SecMgmt
ms.assetid: 697dfecf-46a9-4558-90e2-099fabc60742
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SCESVC_INFO_TYPE, SCESVC_INFO_TYPE enumeration [Security], SceSvcAnalysisInfo, SceSvcConfigurationInfo, SceSvcInternalUse, SceSvcMergedPolicyInfo, _config_scesvc_info_type, scesvc/SCESVC_INFO_TYPE, scesvc/SceSvcAnalysisInfo, scesvc/SceSvcConfigurationInfo, scesvc/SceSvcInternalUse, scesvc/SceSvcMergedPolicyInfo, security.scesvc_info_type
ms.topic: enum
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
 - SCESVC_INFO_TYPE
product: Windows
targetos: Windows
req.typenames: SCESVC_INFO_TYPE
req.redist: 
---

# SCESVC_INFO_TYPE enumeration


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
 

 


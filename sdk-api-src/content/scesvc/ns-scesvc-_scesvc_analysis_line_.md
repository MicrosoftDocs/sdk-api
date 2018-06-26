---
UID: NS:scesvc._SCESVC_ANALYSIS_LINE_
title: "_SCESVC_ANALYSIS_LINE_"
author: windows-sdk-content
description: The SCESVC_ANALYSIS_LINE structure contains the key, value, and value length for a specific line specified by an SCESVC_ANALYSIS_INFO structure.
old-location: security\scesvc_analysis_line.htm
old-project: SecMgmt
ms.assetid: 91fa0f25-30e1-4af3-ad22-f16dc4692b0b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PSCESVC_ANALYSIS_LINE, PSCESVC_ANALYSIS_LINE, PSCESVC_ANALYSIS_LINE structure pointer [Security], SCESVC_ANALYSIS_LINE, SCESVC_ANALYSIS_LINE structure [Security], _SCESVC_ANALYSIS_LINE_, _config_scesvc_analysis_line, scesvc/PSCESVC_ANALYSIS_LINE, scesvc/SCESVC_ANALYSIS_LINE, security.scesvc_analysis_line"
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
req.typenames: SCESVC_ANALYSIS_LINE, *PSCESVC_ANALYSIS_LINE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Scesvc.h
api_name:
 - SCESVC_ANALYSIS_LINE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SCESVC_ANALYSIS_LINE_ structure


## -description


The <b>SCESVC_ANALYSIS_LINE</b> structure contains the key, value, and value length for a specific line specified by an 
<a href="https://msdn.microsoft.com/4f0273df-435d-4324-b8ce-a774da935059">SCESVC_ANALYSIS_INFO</a> structure.


## -struct-fields




### -field Key

String that contains data key. Typically, this is the name of the configuration parameter to which the <b>Value</b> data applies.


### -field Value

Data describing the analysis result for the key. This can be binary data.


### -field ValueLen

Length of the data stored in <b>Value</b>, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/4f0273df-435d-4324-b8ce-a774da935059">SCESVC_ANALYSIS_INFO</a>
 

 


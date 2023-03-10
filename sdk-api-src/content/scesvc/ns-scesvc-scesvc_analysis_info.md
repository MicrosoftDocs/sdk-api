---
UID: NS:scesvc._SCESVC_ANALYSIS_INFO_
title: SCESVC_ANALYSIS_INFO (scesvc.h)
description: Contains the analysis information.
helpviewer_keywords: ["*PSCESVC_ANALYSIS_INFO","PSCESVC_ANALYSIS_INFO","PSCESVC_ANALYSIS_INFO structure pointer [Security]","SCESVC_ANALYSIS_INFO","SCESVC_ANALYSIS_INFO structure [Security]","_config_scesvc_analysis_info","scesvc/PSCESVC_ANALYSIS_INFO","scesvc/SCESVC_ANALYSIS_INFO","security.scesvc_analysis_info"]
old-location: security\scesvc_analysis_info.htm
tech.root: security
ms.assetid: 4f0273df-435d-4324-b8ce-a774da935059
ms.date: 12/05/2018
ms.keywords: '*PSCESVC_ANALYSIS_INFO, PSCESVC_ANALYSIS_INFO, PSCESVC_ANALYSIS_INFO structure pointer [Security], SCESVC_ANALYSIS_INFO, SCESVC_ANALYSIS_INFO structure [Security], _config_scesvc_analysis_info, scesvc/PSCESVC_ANALYSIS_INFO, scesvc/SCESVC_ANALYSIS_INFO, security.scesvc_analysis_info'
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
targetos: Windows
req.typenames: SCESVC_ANALYSIS_INFO, *PSCESVC_ANALYSIS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCESVC_ANALYSIS_INFO_
 - scesvc/_SCESVC_ANALYSIS_INFO_
 - PSCESVC_ANALYSIS_INFO
 - scesvc/PSCESVC_ANALYSIS_INFO
 - SCESVC_ANALYSIS_INFO
 - scesvc/SCESVC_ANALYSIS_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Scesvc.h
api_name:
 - SCESVC_ANALYSIS_INFO
---

# SCESVC_ANALYSIS_INFO structure


## -description

The <b>SCESVC_ANALYSIS_INFO</b> structure contains the analysis information. It contains a 
<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line">SCESVC_ANALYSIS_LINE</a> structure that contains lines of analysis information, and it also contains a counter that indicates the number of lines.

A pointer to this structure is returned by calls to 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a> and 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_set_info">PFSCE_SET_INFO</a> when analysis information is specified.

## -struct-fields

### -field Count

A <b>DWORD</b> that indicates the number of lines in the array.

### -field Lines

Pointer to an array of 
<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line">SCESVC_ANALYSIS_LINE</a> structures which contain the analysis information.

## -see-also

<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a>



<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_set_info">PFSCE_SET_INFO</a>



<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line">SCESVC_ANALYSIS_LINE</a>



<a href="/windows/desktop/api/scesvc/ne-scesvc-scesvc_info_type">SCESVC_INFO_TYPE</a>
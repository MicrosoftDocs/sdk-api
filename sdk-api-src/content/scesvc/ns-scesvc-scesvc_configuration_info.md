---
UID: NS:scesvc._SCESVC_CONFIGURATION_INFO_
title: SCESVC_CONFIGURATION_INFO (scesvc.h)
description: The SCESVC_CONFIGURATION_INFO structure provides configuration information for a service. This structure is used by the PFSCE_QUERY_INFO and PFSCE_SET_INFO functions when the configuration information is specified.
helpviewer_keywords: ["*PSCESVC_CONFIGURATION_INFO","PSCESVC_CONFIGURATION_INFO","PSCESVC_CONFIGURATION_INFO structure pointer [Security]","SCESVC_CONFIGURATION_INFO","SCESVC_CONFIGURATION_INFO structure [Security]","_config_scesvc_configuration_info","scesvc/PSCESVC_CONFIGURATION_INFO","scesvc/SCESVC_CONFIGURATION_INFO","security.scesvc_configuration_info"]
old-location: security\scesvc_configuration_info.htm
tech.root: security
ms.assetid: a89ab072-7b7c-4ecd-83fa-26e2689778df
ms.date: 12/05/2018
ms.keywords: '*PSCESVC_CONFIGURATION_INFO, PSCESVC_CONFIGURATION_INFO, PSCESVC_CONFIGURATION_INFO structure pointer [Security], SCESVC_CONFIGURATION_INFO, SCESVC_CONFIGURATION_INFO structure [Security], _config_scesvc_configuration_info, scesvc/PSCESVC_CONFIGURATION_INFO, scesvc/SCESVC_CONFIGURATION_INFO, security.scesvc_configuration_info'
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
req.typenames: SCESVC_CONFIGURATION_INFO, *PSCESVC_CONFIGURATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCESVC_CONFIGURATION_INFO_
 - scesvc/_SCESVC_CONFIGURATION_INFO_
 - PSCESVC_CONFIGURATION_INFO
 - scesvc/PSCESVC_CONFIGURATION_INFO
 - SCESVC_CONFIGURATION_INFO
 - scesvc/SCESVC_CONFIGURATION_INFO
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
 - SCESVC_CONFIGURATION_INFO
---

# SCESVC_CONFIGURATION_INFO structure


## -description

The <b>SCESVC_CONFIGURATION_INFO</b> structure provides configuration information for a service. This structure is used by the 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a> and 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_set_info">PFSCE_SET_INFO</a> functions when the configuration information is specified.

## -struct-fields

### -field Count

Indicates the number of lines of data returned in the <b>Lines</b> array.

### -field Lines

Pointer to an array of 
<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line">SCESVC_CONFIGURATION_LINE</a> structures which contains the configuration data for this service. Each element represents a line in the security template or database.

## -remarks

When analysis information is specified, the 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a> and 
<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_set_info">PFSCE_SET_INFO</a> functions use the 
<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info">SCESVC_ANALYSIS_INFO</a> structure.

## -see-also

<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a>



<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_set_info">PFSCE_SET_INFO</a>



<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line">SCESVC_CONFIGURATION_LINE</a>



<a href="/windows/desktop/api/scesvc/ne-scesvc-scesvc_info_type">SCESVC_INFO_TYPE</a>
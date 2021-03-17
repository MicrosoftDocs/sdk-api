---
UID: NS:opmapi._OPM_SET_HDCP_SRM_PARAMETERS
title: OPM_SET_HDCP_SRM_PARAMETERS (opmapi.h)
description: Contains parameters for the OPM_SET_HDCP_SRM command.
helpviewer_keywords: ["OPM_SET_HDCP_SRM_PARAMETERS","OPM_SET_HDCP_SRM_PARAMETERS structure [Media Foundation]","mf.opm_set_hdcp_srm_parameters","opmapi/OPM_SET_HDCP_SRM_PARAMETERS"]
old-location: mf\opm_set_hdcp_srm_parameters.htm
tech.root: mf
ms.assetid: 0689e132-8def-43d1-965f-a6f652ad0fbe
ms.date: 12/05/2018
ms.keywords: OPM_SET_HDCP_SRM_PARAMETERS, OPM_SET_HDCP_SRM_PARAMETERS structure [Media Foundation], mf.opm_set_hdcp_srm_parameters, opmapi/OPM_SET_HDCP_SRM_PARAMETERS
req.header: opmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: OPM_SET_HDCP_SRM_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_SET_HDCP_SRM_PARAMETERS
 - opmapi/_OPM_SET_HDCP_SRM_PARAMETERS
 - OPM_SET_HDCP_SRM_PARAMETERS
 - opmapi/OPM_SET_HDCP_SRM_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_SET_HDCP_SRM_PARAMETERS
---

# OPM_SET_HDCP_SRM_PARAMETERS structure


## -description

Contains parameters for the <a href="/windows/desktop/medfound/opm-set-hdcp-srm">OPM_SET_HDCP_SRM</a> command.  This command updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).

## -struct-fields

### -field ulSRMVersion

Contains the SRM version number in little-endian format. This number is contained in the <b>SRM Version</b> field of the SRM. For more information, see the HDCP specification.

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
---
UID: NS:opmapi._OPM_SET_HDCP_SRM_PARAMETERS
title: "_OPM_SET_HDCP_SRM_PARAMETERS"
author: windows-sdk-content
description: Contains parameters for the OPM_SET_HDCP_SRM command.
old-location: mf\opm_set_hdcp_srm_parameters.htm
old-project: medfound
ms.assetid: 0689e132-8def-43d1-965f-a6f652ad0fbe
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: OPM_SET_HDCP_SRM_PARAMETERS, OPM_SET_HDCP_SRM_PARAMETERS structure [Media Foundation], _OPM_SET_HDCP_SRM_PARAMETERS, mf.opm_set_hdcp_srm_parameters, opmapi/OPM_SET_HDCP_SRM_PARAMETERS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: OPM_SET_HDCP_SRM_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_SET_HDCP_SRM_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _OPM_SET_HDCP_SRM_PARAMETERS structure


## -description


Contains parameters for the <a href="https://msdn.microsoft.com/ea18baba-0e03-4471-af0e-a588773c98d2">OPM_SET_HDCP_SRM</a> command.  This command updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).
      


## -struct-fields




### -field ulSRMVersion

Contains the SRM version number in little-endian format. This number is contained in the <b>SRM Version</b> field of the SRM. For more information, see the HDCP specification.


## -see-also




<a href="https://msdn.microsoft.com/676a60ca-393e-4b5d-89d3-50cf4b771492">OPM Structures</a>



<a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>
 

 


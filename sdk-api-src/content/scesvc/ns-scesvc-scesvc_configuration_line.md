---
UID: NS:scesvc._SCESVC_CONFIGURATION_LINE_
title: SCESVC_CONFIGURATION_LINE (scesvc.h)
description: The SCESVC_CONFIGURATION_LINE structure contains information about a line of configuration data. It is used by the SCESVC_CONFIGURATION_INFO structure.
helpviewer_keywords: ["*PSCESVC_CONFIGURATION_LINE","PSCESVC_CONFIGURATION_LINE","PSCESVC_CONFIGURATION_LINE structure pointer [Security]","SCESVC_CONFIGURATION_LINE","SCESVC_CONFIGURATION_LINE structure [Security]","_config_scesvc_configuration_line","scesvc/PSCESVC_CONFIGURATION_LINE","scesvc/SCESVC_CONFIGURATION_LINE","security.scesvc_configuration_line"]
old-location: security\scesvc_configuration_line.htm
tech.root: security
ms.assetid: 25801b20-9a7a-423e-8fa3-86896a8fbae4
ms.date: 12/05/2018
ms.keywords: '*PSCESVC_CONFIGURATION_LINE, PSCESVC_CONFIGURATION_LINE, PSCESVC_CONFIGURATION_LINE structure pointer [Security], SCESVC_CONFIGURATION_LINE, SCESVC_CONFIGURATION_LINE structure [Security], _config_scesvc_configuration_line, scesvc/PSCESVC_CONFIGURATION_LINE, scesvc/SCESVC_CONFIGURATION_LINE, security.scesvc_configuration_line'
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
req.typenames: SCESVC_CONFIGURATION_LINE, *PSCESVC_CONFIGURATION_LINE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCESVC_CONFIGURATION_LINE_
 - scesvc/_SCESVC_CONFIGURATION_LINE_
 - PSCESVC_CONFIGURATION_LINE
 - scesvc/PSCESVC_CONFIGURATION_LINE
 - SCESVC_CONFIGURATION_LINE
 - scesvc/SCESVC_CONFIGURATION_LINE
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
 - SCESVC_CONFIGURATION_LINE
---

# SCESVC_CONFIGURATION_LINE structure


## -description

The <b>SCESVC_CONFIGURATION_LINE</b> structure contains information about a line of configuration data. It is used by the 
<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info">SCESVC_CONFIGURATION_INFO</a> structure.

## -struct-fields

### -field Key

String that contains data key. Typically this is the name of the configuration parameter to which the <b>Value</b> data applies.

### -field Value

String that contains data describing the configuration.

### -field ValueLen

Length of the data stored in <b>Value</b>, in bytes.

## -see-also

<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info">SCESVC_CONFIGURATION_INFO</a>


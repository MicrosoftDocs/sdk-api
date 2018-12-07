---
UID: NS:scesvc._SCESVC_CONFIGURATION_LINE_
title: "_SCESVC_CONFIGURATION_LINE_"
author: windows-sdk-content
description: The SCESVC_CONFIGURATION_LINE structure contains information about a line of configuration data. It is used by the SCESVC_CONFIGURATION_INFO structure.
old-location: security\scesvc_configuration_line.htm
tech.root: secmgmt
ms.assetid: 25801b20-9a7a-423e-8fa3-86896a8fbae4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSCESVC_CONFIGURATION_LINE, PSCESVC_CONFIGURATION_LINE, PSCESVC_CONFIGURATION_LINE structure pointer [Security], SCESVC_CONFIGURATION_LINE, SCESVC_CONFIGURATION_LINE structure [Security], _SCESVC_CONFIGURATION_LINE_, _config_scesvc_configuration_line, scesvc/PSCESVC_CONFIGURATION_LINE, scesvc/SCESVC_CONFIGURATION_LINE, security.scesvc_configuration_line"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SCESVC_CONFIGURATION_LINE
product: Windows
targetos: Windows
req.typenames: SCESVC_CONFIGURATION_LINE, *PSCESVC_CONFIGURATION_LINE
req.redist: 
---

# _SCESVC_CONFIGURATION_LINE_ structure


## -description


The <b>SCESVC_CONFIGURATION_LINE</b> structure contains information about a line of configuration data. It is used by the 
<a href="https://msdn.microsoft.com/a89ab072-7b7c-4ecd-83fa-26e2689778df">SCESVC_CONFIGURATION_INFO</a> structure.


## -struct-fields




### -field Key

String that contains data key. Typically this is the name of the configuration parameter to which the <b>Value</b> data applies.


### -field Value

String that contains data describing the configuration.


### -field ValueLen

Length of the data stored in <b>Value</b>, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/a89ab072-7b7c-4ecd-83fa-26e2689778df">SCESVC_CONFIGURATION_INFO</a>
 

 


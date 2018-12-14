---
UID: NS:wsdbase._WSD_CONFIG_PARAM
title: WSD_CONFIG_PARAM
author: windows-sdk-content
description: Represents configuration parameters for creating WSDAPI objects.
old-location: ncd\wsd_config_param.htm
tech.root: wsdapi
ms.assetid: 58dc3e11-586e-4185-b1d0-4249b4bfb252
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWSD_CONFIG_PARAM, WSD_CONFIG_PARAM, WSD_CONFIG_PARAM structure, _WSD_CONFIG_PARAM, ncd.wsd_config_param, wsdbase/WSD_CONFIG_PARAM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - wsdbase.h
api_name:
 - WSD_CONFIG_PARAM
product: Windows
targetos: Windows
req.typenames: WSD_CONFIG_PARAM, *PWSD_CONFIG_PARAM
req.redist: 
---

# WSD_CONFIG_PARAM structure


## -description


Represents configuration parameters for creating <code>WSDAPI</code> objects.


## -struct-fields




### -field configParamType

A <a href="https://msdn.microsoft.com/46189d61-79d0-4ec9-82eb-ac1331201490">WSD_CONFIG_PARAM_TYPE</a> value that indicates the type configuration data contained in this structure.


### -field pConfigData

A pointer to a single configuration data structure.   The <i>configParamType</i> member specifies the type of data passed in.


### -field dwConfigDataSize

The size of the configuration data in <i>pConfigData</i>.


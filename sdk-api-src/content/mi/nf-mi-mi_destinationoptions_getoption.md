---
UID: NF:mi.MI_DestinationOptions_GetOption
title: MI_DestinationOptions_GetOption function (mi.h)
description: Gets a previously added option value based on the option name. (MI_DestinationOptions_GetOption)
helpviewer_keywords: ["MI_DestinationOptions_GetOption","MI_DestinationOptions_GetOption function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetOption","wmi_v2.mi_destinationoptions_getoption"]
old-location: wmi_v2\mi_destinationoptions_getoption.htm
tech.root: wmi_v2
ms.assetid: f7f26a4f-109f-4169-bc77-b0c763d7bcb8
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetOption, MI_DestinationOptions_GetOption function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetOption, wmi_v2.mi_destinationoptions_getoption
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_DestinationOptions_GetOption
 - mi/MI_DestinationOptions_GetOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_DestinationOptions_GetOption
---

# MI_DestinationOptions_GetOption function


## -description

Gets a previously added option value based on the option name.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param optionName

A null-terminated string that represents the name of the option to get.

### -param value [out]

The returned option value. This value is owned by the destination options object, so there is no need to delete it.

### -param type [out]

Returned option type.

### -param index [out, optional]

Returned zero-based index of the option.

### -param flags [out, optional]

Returned option flags.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

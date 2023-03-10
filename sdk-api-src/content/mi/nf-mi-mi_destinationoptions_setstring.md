---
UID: NF:mi.MI_DestinationOptions_SetString
title: MI_DestinationOptions_SetString function (mi.h)
description: Sets a custom string option. (MI_DestinationOptions_SetString)
helpviewer_keywords: ["MI_DestinationOptions_SetString","MI_DestinationOptions_SetString function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetString","wmi_v2.mi_destinationoptions_setstring"]
old-location: wmi_v2\mi_destinationoptions_setstring.htm
tech.root: wmi_v2
ms.assetid: 40621d0b-3ff2-4960-8cb0-e95bad0d08db
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetString, MI_DestinationOptions_SetString function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetString, wmi_v2.mi_destinationoptions_setstring
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
 - MI_DestinationOptions_SetString
 - mi/MI_DestinationOptions_SetString
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
 - MI_DestinationOptions_SetString
---

# MI_DestinationOptions_SetString function


## -description

Sets a custom string option.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param optionName

A null-terminated string that represents the name of the option to set.

### -param optionValue

A null-terminated string that represents the new value of the option.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getstring">MI_DestinationOptions_GetString</a>

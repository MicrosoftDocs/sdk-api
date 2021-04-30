---
UID: NF:mi.MI_DestinationOptions_GetString
title: MI_DestinationOptions_GetString function (mi.h)
description: Gets a previously added custom string option.
helpviewer_keywords: ["MI_DestinationOptions_GetString","MI_DestinationOptions_GetString function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetString","wmi_v2.mi_destinationoptions_getstring"]
old-location: wmi_v2\mi_destinationoptions_getstring.htm
tech.root: wmi_v2
ms.assetid: 49bd7fa6-0164-4fb6-8154-75c39e6f7858
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetString, MI_DestinationOptions_GetString function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetString, wmi_v2.mi_destinationoptions_getstring
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
 - MI_DestinationOptions_GetString
 - mi/MI_DestinationOptions_GetString
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
 - MI_DestinationOptions_GetString
---

# MI_DestinationOptions_GetString function


## -description

Gets a previously added custom string option.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param optionName

A null-terminated string that represents the name of the option to get.

### -param optionValue

A pointer to a null-terminated string containing the returned option value. This value is owned by the <i>options</i> parameter, so it does not need to be deleted.

### -param index [out, optional]

Returned zero-based index of value.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_setstring">MI_DestinationOptions_SetString</a>
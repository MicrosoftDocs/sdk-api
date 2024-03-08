---
UID: NF:mi.MI_DestinationOptions_GetNumber
title: MI_DestinationOptions_GetNumber function (mi.h)
description: Gets a previously added custom number option. (MI_DestinationOptions_GetNumber)
helpviewer_keywords: ["MI_DestinationOptions_GetNumber","MI_DestinationOptions_GetNumber function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetNumber","wmi_v2.mi_destinationoptions_getnumber"]
old-location: wmi_v2\mi_destinationoptions_getnumber.htm
tech.root: wmi_v2
ms.assetid: ac48c290-631f-427e-a544-ee0258029c42
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetNumber, MI_DestinationOptions_GetNumber function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetNumber, wmi_v2.mi_destinationoptions_getnumber
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
 - MI_DestinationOptions_GetNumber
 - mi/MI_DestinationOptions_GetNumber
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
 - MI_DestinationOptions_GetNumber
---

# MI_DestinationOptions_GetNumber function


## -description

Gets a previously added custom number option.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param optionName

A null-terminated string that represents the name of the option to get.

### -param optionValue [out]

Returned option value.

### -param index [out, optional]

Returned zero-based index of the option.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

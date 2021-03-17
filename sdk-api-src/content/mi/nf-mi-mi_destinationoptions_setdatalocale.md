---
UID: NF:mi.MI_DestinationOptions_SetDataLocale
title: MI_DestinationOptions_SetDataLocale function (mi.h)
description: Sets the default data locale to use for operations.
helpviewer_keywords: ["MI_DestinationOptions_SetDataLocale","MI_DestinationOptions_SetDataLocale function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetDataLocale","wmi_v2.mi_destinationoptions_setdatalocale"]
old-location: wmi_v2\mi_destinationoptions_setdatalocale.htm
tech.root: wmi_v2
ms.assetid: 0b5c0ae7-d11c-4014-b61e-4528b9320844
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetDataLocale, MI_DestinationOptions_SetDataLocale function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetDataLocale, wmi_v2.mi_destinationoptions_setdatalocale
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
 - MI_DestinationOptions_SetDataLocale
 - mi/MI_DestinationOptions_SetDataLocale
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
 - MI_DestinationOptions_SetDataLocale
---

# MI_DestinationOptions_SetDataLocale function


## -description

Sets the default data locale to use for operations.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param locale

A null-terminated string that represents the new data locale string (for example, "en-us").

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

Data locale represents the format of date strings, whether a dot or a comma is used in floating-point numbers, and a number of other locale specific data.  By default, the data locale set on the impersonation thread will be used for the operation unless overridden via this function.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getdatalocale">MI_DestinationOptions_GetDataLocale</a>
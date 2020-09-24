---
UID: NF:mi.MI_DestinationOptions_SetUILocale
title: MI_DestinationOptions_SetUILocale function (mi.h)
description: Sets the default UI locale for operations.
helpviewer_keywords: ["MI_DestinationOptions_SetUILocale","MI_DestinationOptions_SetUILocale function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetUILocale","wmi_v2.mi_destinationoptions_setuilocale"]
old-location: wmi_v2\mi_destinationoptions_setuilocale.htm
tech.root: wmi_v2
ms.assetid: a536544c-003b-402e-9d63-d3e30b49cc39
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetUILocale, MI_DestinationOptions_SetUILocale function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetUILocale, wmi_v2.mi_destinationoptions_setuilocale
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
 - MI_DestinationOptions_SetUILocale
 - mi/MI_DestinationOptions_SetUILocale
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
 - MI_DestinationOptions_SetUILocale
---

# MI_DestinationOptions_SetUILocale function


## -description

Sets the default UI locale for operations.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param locale

A null-terminated string that represents the locale string to be used (for example, "en-us").

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

The UI locale represents the language that error messages should come back to the client in.  By default, the UI locale of the calling thread for the execution of an operation would be used.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getuilocale">MI_DestinationOptions_GetUILocale</a>
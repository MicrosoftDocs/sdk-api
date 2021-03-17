---
UID: NF:mi.MI_DestinationOptions_GetUILocale
title: MI_DestinationOptions_GetUILocale function (mi.h)
description: Gets the user interface locale set by the user.
helpviewer_keywords: ["MI_DestinationOptions_GetUILocale","MI_DestinationOptions_GetUILocale function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetUILocale","wmi_v2.mi_destinationoptions_getuilocale"]
old-location: wmi_v2\mi_destinationoptions_getuilocale.htm
tech.root: wmi_v2
ms.assetid: c05104c8-ecf7-447c-9cea-25a26b82bc69
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetUILocale, MI_DestinationOptions_GetUILocale function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetUILocale, wmi_v2.mi_destinationoptions_getuilocale
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
 - MI_DestinationOptions_GetUILocale
 - mi/MI_DestinationOptions_GetUILocale
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
 - MI_DestinationOptions_GetUILocale
---

# MI_DestinationOptions_GetUILocale function


## -description

Gets the user interface locale set by the user.

## -parameters

### -param options [in]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param locale

A pointer to a null-terminated string containing the returned locale setting. This setting is owned by the <i>options</i> parameter, so there is no need to delete the locale.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_setuilocale">MI_DestinationOptions_SetUILocale</a>
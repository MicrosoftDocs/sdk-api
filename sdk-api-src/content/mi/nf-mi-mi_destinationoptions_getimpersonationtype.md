---
UID: NF:mi.MI_DestinationOptions_GetImpersonationType
title: MI_DestinationOptions_GetImpersonationType function (mi.h)
description: Gets the impersonation type.
helpviewer_keywords: ["MI_DestinationOptions_GetImpersonationType","MI_DestinationOptions_GetImpersonationType function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetImpersonationType","wmi_v2.mi_destinationoptions_getimpersonationtype"]
old-location: wmi_v2\mi_destinationoptions_getimpersonationtype.htm
tech.root: wmi_v2
ms.assetid: 3178e69c-83da-4ffb-8d8e-9185b669e864
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetImpersonationType, MI_DestinationOptions_GetImpersonationType function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetImpersonationType, wmi_v2.mi_destinationoptions_getimpersonationtype
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
 - MI_DestinationOptions_GetImpersonationType
 - mi/MI_DestinationOptions_GetImpersonationType
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
 - MI_DestinationOptions_GetImpersonationType
---

# MI_DestinationOptions_GetImpersonationType function


## -description

Gets the impersonation type.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param impersonationType [out]

Returned <a href="/windows/desktop/api/mi/ne-mi-mi_destinationoptions_impersonationtype">MI_DestinationOptions_ImpersonationType</a> enumeration.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
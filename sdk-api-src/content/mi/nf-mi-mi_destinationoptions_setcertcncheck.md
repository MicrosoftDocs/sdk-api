---
UID: NF:mi.MI_DestinationOptions_SetCertCNCheck
title: MI_DestinationOptions_SetCertCNCheck function (mi.h)
description: Enables or disables the certificate CN check when an SSL transport is used.
helpviewer_keywords: ["MI_DestinationOptions_SetCertCNCheck","MI_DestinationOptions_SetCertCNCheck function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetCertCNCheck","wmi_v2.mi_destinationoptions_setcertcncheck"]
old-location: wmi_v2\mi_destinationoptions_setcertcncheck.htm
tech.root: wmi_v2
ms.assetid: 19b8bcf5-192a-4e14-9efe-3124b8051e04
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetCertCNCheck, MI_DestinationOptions_SetCertCNCheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetCertCNCheck, wmi_v2.mi_destinationoptions_setcertcncheck
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
 - MI_DestinationOptions_SetCertCNCheck
 - mi/MI_DestinationOptions_SetCertCNCheck
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
 - MI_DestinationOptions_SetCertCNCheck
---

# MI_DestinationOptions_SetCertCNCheck function


## -description

Enables or disables the certificate CN check when an SSL transport is used.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param check

Boolean value where <b>MI_TRUE</b> means to enable the certificate CN check and <b>MI_FALSE</b> means to disable it.

## -remarks

The certificate CN is checked by default.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getcertcncheck">MI_DestinationOptions_GetCertCNCheck</a>
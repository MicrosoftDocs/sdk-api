---
UID: NF:mi.MI_DestinationOptions_GetCertCACheck
title: MI_DestinationOptions_GetCertCACheck function (mi.h)
description: Gets the server certificate CA check value.
helpviewer_keywords: ["MI_DestinationOptions_GetCertCACheck","MI_DestinationOptions_GetCertCACheck function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetCertCACheck","wmi_v2.mi_destinationoptions_getcertcacheck"]
old-location: wmi_v2\mi_destinationoptions_getcertcacheck.htm
tech.root: wmi_v2
ms.assetid: 9b1b5bca-4e1f-4c37-9df4-9101f40f1b97
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetCertCACheck, MI_DestinationOptions_GetCertCACheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetCertCACheck, wmi_v2.mi_destinationoptions_getcertcacheck
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
 - MI_DestinationOptions_GetCertCACheck
 - mi/MI_DestinationOptions_GetCertCACheck
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
 - MI_DestinationOptions_GetCertCACheck
---

# MI_DestinationOptions_GetCertCACheck function


## -description

Gets the server certificate CA check value.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param check [out]

Returned Boolean value indicating if the CA value will be checked (<b>MI_TRUE</b>) or not (<b>MI_FALSE</b>).

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

All getters only return information that was previously added by the client. This is appropriate to all the getters of destination and operation options.
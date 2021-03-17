---
UID: NF:mi.MI_DestinationOptions_GetCertRevocationCheck
title: MI_DestinationOptions_GetCertRevocationCheck function (mi.h)
description: Gets the server certificate's revocation check value.
helpviewer_keywords: ["MI_DestinationOptions_GetCertRevocationCheck","MI_DestinationOptions_GetCertRevocationCheck function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_GetCertRevocationCheck","wmi_v2.mi_destinationoptions_getcertrevocationcheck"]
old-location: wmi_v2\mi_destinationoptions_getcertrevocationcheck.htm
tech.root: wmi_v2
ms.assetid: 85af8514-a448-44c4-b1ad-f0a6b5c4a8a4
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_GetCertRevocationCheck, MI_DestinationOptions_GetCertRevocationCheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_GetCertRevocationCheck, wmi_v2.mi_destinationoptions_getcertrevocationcheck
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
 - MI_DestinationOptions_GetCertRevocationCheck
 - mi/MI_DestinationOptions_GetCertRevocationCheck
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
 - MI_DestinationOptions_GetCertRevocationCheck
---

# MI_DestinationOptions_GetCertRevocationCheck function


## -description

Gets the server certificate's revocation check value.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param check [out]

Returned revocation check value where <b>MI_TRUE</b> means that the revocation check will occur and <b>MI_FALSE</b> meaning that it won't.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
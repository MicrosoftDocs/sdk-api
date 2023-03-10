---
UID: NF:mi.MI_DestinationOptions_SetCertRevocationCheck
title: MI_DestinationOptions_SetCertRevocationCheck function (mi.h)
description: Enables or disables the certificate revocation when communicating over SSL.
helpviewer_keywords: ["MI_DestinationOptions_SetCertRevocationCheck","MI_DestinationOptions_SetCertRevocationCheck function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetCertRevocationCheck","wmi_v2.mi_destinationoptions_setcertrevocationcheck"]
old-location: wmi_v2\mi_destinationoptions_setcertrevocationcheck.htm
tech.root: wmi_v2
ms.assetid: 941d1649-a4b1-4160-9917-a94afe0b8cd6
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetCertRevocationCheck, MI_DestinationOptions_SetCertRevocationCheck function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetCertRevocationCheck, wmi_v2.mi_destinationoptions_setcertrevocationcheck
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
 - MI_DestinationOptions_SetCertRevocationCheck
 - mi/MI_DestinationOptions_SetCertRevocationCheck
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
 - MI_DestinationOptions_SetCertRevocationCheck
---

# MI_DestinationOptions_SetCertRevocationCheck function


## -description

Enables or disables the certificate revocation when communicating over SSL.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>.

### -param check

A Boolean value, where <b>MI_TRUE</b> means the server's certificate will be checked for revocation, while <b>MI_FALSE</b> means the certificate will not be checked.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getcertrevocationcheck">MI_DestinationOptions_GetCertRevocationCheck</a>
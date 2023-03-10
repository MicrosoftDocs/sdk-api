---
UID: NE:mi._MI_DestinationOptions_ImpersonationType
title: MI_DestinationOptions_ImpersonationType (mi.h)
description: Used by the DCOM protocol handler to specify how impersonation is done on the server.
helpviewer_keywords: ["MI_DestinationOptions_ImpersonationType","MI_DestinationOptions_ImpersonationType enumeration [Windows Management Infrastructure (MI)]","MI_DestinationOptions_ImpersonationType_Default","MI_DestinationOptions_ImpersonationType_Delegate","MI_DestinationOptions_ImpersonationType_Identify","MI_DestinationOptions_ImpersonationType_Impersonate","MI_DestinationOptions_ImpersonationType_None","mi/MI_DestinationOptions_ImpersonationType","mi/MI_DestinationOptions_ImpersonationType_Default","mi/MI_DestinationOptions_ImpersonationType_Delegate","mi/MI_DestinationOptions_ImpersonationType_Identify","mi/MI_DestinationOptions_ImpersonationType_Impersonate","mi/MI_DestinationOptions_ImpersonationType_None","wmi._mi_destinationoptions_impersonationtype","wmi_v2.mi_destinationoptions_impersonationtype"]
old-location: wmi_v2\mi_destinationoptions_impersonationtype.htm
tech.root: wmi_v2
ms.assetid: 3d78ca66-8807-45b2-8648-bc5b0dfb83c6
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_ImpersonationType, MI_DestinationOptions_ImpersonationType enumeration [Windows Management Infrastructure (MI)], MI_DestinationOptions_ImpersonationType_Default, MI_DestinationOptions_ImpersonationType_Delegate, MI_DestinationOptions_ImpersonationType_Identify, MI_DestinationOptions_ImpersonationType_Impersonate, MI_DestinationOptions_ImpersonationType_None, mi/MI_DestinationOptions_ImpersonationType, mi/MI_DestinationOptions_ImpersonationType_Default, mi/MI_DestinationOptions_ImpersonationType_Delegate, mi/MI_DestinationOptions_ImpersonationType_Identify, mi/MI_DestinationOptions_ImpersonationType_Impersonate, mi/MI_DestinationOptions_ImpersonationType_None, wmi._mi_destinationoptions_impersonationtype, wmi_v2.mi_destinationoptions_impersonationtype
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
req.typenames: MI_DestinationOptions_ImpersonationType
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_DestinationOptions_ImpersonationType
 - mi/_MI_DestinationOptions_ImpersonationType
 - MI_DestinationOptions_ImpersonationType
 - mi/MI_DestinationOptions_ImpersonationType
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
 - MI_DestinationOptions_ImpersonationType
---

# MI_DestinationOptions_ImpersonationType enumeration


## -description

Used by the DCOM protocol handler to specify how impersonation is done on the server.

## -enum-fields

### -field MI_DestinationOptions_ImpersonationType_Default:0

Use the default impersonation.

### -field MI_DestinationOptions_ImpersonationType_None:1

Do not impersonate.

### -field MI_DestinationOptions_ImpersonationType_Identify:2

Identify user only.

### -field MI_DestinationOptions_ImpersonationType_Impersonate:3

Allow impersonation of user.

### -field MI_DestinationOptions_ImpersonationType_Delegate:4

This option relates to Kerberos delegation and needs to be enabled on the domain.


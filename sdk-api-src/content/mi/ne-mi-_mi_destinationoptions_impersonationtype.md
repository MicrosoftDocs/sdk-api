---
UID: NE:mi._MI_DestinationOptions_ImpersonationType
title: "_MI_DestinationOptions_ImpersonationType"
author: windows-driver-content
description: Used by the DCOM protocol handler to specify how impersonation is done on the server.
old-location: wmi_v2\mi_destinationoptions_impersonationtype.htm
old-project: wmi_v2
ms.assetid: 3d78ca66-8807-45b2-8648-bc5b0dfb83c6
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: MI_DestinationOptions_ImpersonationType, MI_DestinationOptions_ImpersonationType enumeration [Windows Management Infrastructure (MI)], MI_DestinationOptions_ImpersonationType_Default, MI_DestinationOptions_ImpersonationType_Delegate, MI_DestinationOptions_ImpersonationType_Identify, MI_DestinationOptions_ImpersonationType_Impersonate, MI_DestinationOptions_ImpersonationType_None, _MI_DestinationOptions_ImpersonationType, mi/MI_DestinationOptions_ImpersonationType, mi/MI_DestinationOptions_ImpersonationType_Default, mi/MI_DestinationOptions_ImpersonationType_Delegate, mi/MI_DestinationOptions_ImpersonationType_Identify, mi/MI_DestinationOptions_ImpersonationType_Impersonate, mi/MI_DestinationOptions_ImpersonationType_None, wmi._mi_destinationoptions_impersonationtype, wmi_v2.mi_destinationoptions_impersonationtype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: MI_DestinationOptions_ImpersonationType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_DestinationOptions_ImpersonationType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_DestinationOptions_ImpersonationType enumeration


## -description


Used by the DCOM protocol handler to specify how impersonation is done on the server.


## -enum-fields




### -field MI_DestinationOptions_ImpersonationType_Default

Use the default impersonation.


### -field MI_DestinationOptions_ImpersonationType_None

Do not impersonate.


### -field MI_DestinationOptions_ImpersonationType_Identify

Identify user only.


### -field MI_DestinationOptions_ImpersonationType_Impersonate

Allow impersonation of user.


### -field MI_DestinationOptions_ImpersonationType_Delegate

This option relates to Kerberos delegation and needs to be enabled on the domain.


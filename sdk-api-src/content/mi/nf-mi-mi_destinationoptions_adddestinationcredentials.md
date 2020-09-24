---
UID: NF:mi.MI_DestinationOptions_AddDestinationCredentials
title: MI_DestinationOptions_AddDestinationCredentials function (mi.h)
description: Sets the credentials for talking to the destination.
helpviewer_keywords: ["MI_DestinationOptions_AddDestinationCredentials","MI_DestinationOptions_AddDestinationCredentials function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_AddDestinationCredentials","wmi_v2.mi_destinationoptions_adddestinationcredentials"]
old-location: wmi_v2\mi_destinationoptions_adddestinationcredentials.htm
tech.root: wmi_v2
ms.assetid: d3abb931-47eb-4f13-b463-caf6c6b918b0
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_AddDestinationCredentials, MI_DestinationOptions_AddDestinationCredentials function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_AddDestinationCredentials, wmi_v2.mi_destinationoptions_adddestinationcredentials
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
 - MI_DestinationOptions_AddDestinationCredentials
 - mi/MI_DestinationOptions_AddDestinationCredentials
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
 - MI_DestinationOptions_AddDestinationCredentials
---

# MI_DestinationOptions_AddDestinationCredentials function


## -description

Sets the credentials for talking to the destination.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> structure that contains the destination options.

### -param credentials [in]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_usercredentials">MI_UserCredentials</a> structure that contains the credentials used when communicating with the destination machine.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

The credentials supported will vary depending on the destination, the protocol and the transport.  If dual-factor authentication is required this method can be called twice.  The default credentials will vary depending on the protocol and transport selected.
---
UID: NF:mi.MI_DestinationOptions_SetPacketIntegrity
title: MI_DestinationOptions_SetPacketIntegrity function (mi.h)
description: Enables or disables packet integrity (signing) of a protocol connection.
helpviewer_keywords: ["MI_DestinationOptions_SetPacketIntegrity","MI_DestinationOptions_SetPacketIntegrity function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetPacketIntegrity","wmi_v2.mi_destinationoptions_setpacketintegrity"]
old-location: wmi_v2\mi_destinationoptions_setpacketintegrity.htm
tech.root: wmi_v2
ms.assetid: 62980401-84ba-40af-a0c0-36d24c4d68f4
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetPacketIntegrity, MI_DestinationOptions_SetPacketIntegrity function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetPacketIntegrity, wmi_v2.mi_destinationoptions_setpacketintegrity
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
 - MI_DestinationOptions_SetPacketIntegrity
 - mi/MI_DestinationOptions_SetPacketIntegrity
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
 - MI_DestinationOptions_SetPacketIntegrity
---

# MI_DestinationOptions_SetPacketIntegrity function


## -description

Enables or disables packet integrity (signing) of a protocol connection.

## -parameters

### -param options [in, out]

A <a href="/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.

### -param integrity

Boolean value where <b>MI_TRUE</b> means to use packet integrity (signing) and <b>MI_FALSE</b> means to not use packet integrity.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

The default setting is <b>MI_TRUE</b>. This setting does not apply to all protocols and will be ignored when not supported.
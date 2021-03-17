---
UID: NF:mi.MI_OperationOptions_DisableChannel
title: MI_OperationOptions_DisableChannel function (mi.h)
description: Uses MI_Context_WriteMessage to disable logging to the specified channel.
helpviewer_keywords: ["MI_OperationOptions_DisableChannel","MI_OperationOptions_DisableChannel function [Windows Management Infrastructure (MI)]","MI_WRITEMESSAGE_CHANNEL_DEBUG","MI_WRITEMESSAGE_CHANNEL_VERBOSE","MI_WRITEMESSAGE_CHANNEL_WARNING","mi/MI_OperationOptions_DisableChannel","wmi_v2.mi_operationoptions_disablechannel"]
old-location: wmi_v2\mi_operationoptions_disablechannel.htm
tech.root: wmi_v2
ms.assetid: fed7893b-16cb-4c51-a8dc-68440f358712
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_DisableChannel, MI_OperationOptions_DisableChannel function [Windows Management Infrastructure (MI)], MI_WRITEMESSAGE_CHANNEL_DEBUG, MI_WRITEMESSAGE_CHANNEL_VERBOSE, MI_WRITEMESSAGE_CHANNEL_WARNING, mi/MI_OperationOptions_DisableChannel, wmi_v2.mi_operationoptions_disablechannel
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
 - MI_OperationOptions_DisableChannel
 - mi/MI_OperationOptions_DisableChannel
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
 - MI_OperationOptions_DisableChannel
---

# MI_OperationOptions_DisableChannel function


## -description

Uses <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_context_writemessage">MI_Context_WriteMessage</a> to disable logging to the specified 
     channel.

## -parameters

### -param options [in, out]

A pointer to a <a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param channel [in]

Channel to disable, which can be any of the following.



#### MI_WRITEMESSAGE_CHANNEL_WARNING

Channel used to broadcast warning messages.



#### MI_WRITEMESSAGE_CHANNEL_VERBOSE

Channel used to broadcast verbose informational messages.



#### MI_WRITEMESSAGE_CHANNEL_DEBUG

Channel used to broadcast debugging information.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
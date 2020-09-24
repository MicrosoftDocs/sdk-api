---
UID: NF:mi.MI_OperationOptions_GetEnabledChannels
title: MI_OperationOptions_GetEnabledChannels function (mi.h)
description: Gets the list of previously enabled channels.
helpviewer_keywords: ["MI_OperationOptions_GetEnabledChannels","MI_OperationOptions_GetEnabledChannels function [Windows Management Infrastructure (MI)]","mi/MI_OperationOptions_GetEnabledChannels","wmi_v2.mi_operationoptions_getenabledchannels"]
old-location: wmi_v2\mi_operationoptions_getenabledchannels.htm
tech.root: wmi_v2
ms.assetid: 5604288f-cc51-40b2-b9a8-5d972e05b172
ms.date: 12/05/2018
ms.keywords: MI_OperationOptions_GetEnabledChannels, MI_OperationOptions_GetEnabledChannels function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetEnabledChannels, wmi_v2.mi_operationoptions_getenabledchannels
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
 - MI_OperationOptions_GetEnabledChannels
 - mi/MI_OperationOptions_GetEnabledChannels
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
 - MI_OperationOptions_GetEnabledChannels
---

# MI_OperationOptions_GetEnabledChannels function


## -description

Gets the list of previously enabled channels.

## -parameters

### -param options [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_operationoptions">MI_OperationOptions</a> structure.

### -param channels

Returned buffer that contains the numbers of all enabled channels.

### -param bufferLength [in]

The length, in elements, of the <b>channels</b> buffer. If 0, the returned <b>channelCount</b> value will reflect how large the <b>channels</b> buffer needs to be.

### -param channelCount [out]

Number of enabled channels.

### -param flags [out, optional]

Unused.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
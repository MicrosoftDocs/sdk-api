---
UID: NF:mi.MI_OperationOptions_GetEnabledChannels
title: MI_OperationOptions_GetEnabledChannels function
author: windows-sdk-content
description: Gets the list of previously enabled channels.
old-location: wmi_v2\mi_operationoptions_getenabledchannels.htm
tech.root: WMI_v2
ms.assetid: 5604288f-cc51-40b2-b9a8-5d972e05b172
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_OperationOptions_GetEnabledChannels, MI_OperationOptions_GetEnabledChannels function [Windows Management Infrastructure (MI)], mi/MI_OperationOptions_GetEnabledChannels, wmi_v2.mi_operationoptions_getenabledchannels
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationOptions_GetEnabledChannels
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_OperationOptions_GetEnabledChannels function


## -description


Gets the list of previously enabled channels.


## -parameters




### -param options [in]


<a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param channels

Returned buffer that contains the numbers of all enabled channels.


### -param bufferLength [in]

The length, in elements, of the <b>channels</b> buffer. If 0, the returned <b>channelCount</b> value will reflect how large the <b>channels</b> buffer needs to be.


### -param channelCount [out]

Number of enabled channels.


### -param flags [out, optional]

Unused.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




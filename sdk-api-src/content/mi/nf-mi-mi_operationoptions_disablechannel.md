---
UID: NF:mi.MI_OperationOptions_DisableChannel
title: MI_OperationOptions_DisableChannel function
author: windows-sdk-content
description: Uses MI_Context_WriteMessage to disable logging to the specified channel.
old-location: wmi_v2\mi_operationoptions_disablechannel.htm
old-project: wmi_v2
ms.assetid: fed7893b-16cb-4c51-a8dc-68440f358712
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_OperationOptions_DisableChannel, MI_OperationOptions_DisableChannel function [Windows Management Infrastructure (MI)], MI_WRITEMESSAGE_CHANNEL_DEBUG, MI_WRITEMESSAGE_CHANNEL_VERBOSE, MI_WRITEMESSAGE_CHANNEL_WARNING, mi/MI_OperationOptions_DisableChannel, wmi_v2.mi_operationoptions_disablechannel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_OperationOptions_DisableChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_OperationOptions_DisableChannel function


## -description


Uses <a href="https://msdn.microsoft.com/2e4dbb4d-5482-4ed0-9903-34b3bb87b16f">MI_Context_WriteMessage</a> to disable logging to the specified 
     channel.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> structure.


### -param channel [in]

Channel to disable, which can be any of the following.



#### MI_WRITEMESSAGE_CHANNEL_WARNING

Channel used to broadcast warning messages.



#### MI_WRITEMESSAGE_CHANNEL_VERBOSE

Channel used to broadcast verbose informational messages.



#### MI_WRITEMESSAGE_CHANNEL_DEBUG

Channel used to broadcast debugging information.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



